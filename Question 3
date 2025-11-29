class FileDownload extends Thread {
    private String part;

    public FileDownload(String part) {
        this.part = part;
    }

    public void run() {
        try {
            System.out.println(part + " downloading...");
            Thread.sleep(2000);
            System.out.println(part + " completed.");
        } catch (InterruptedException e) {
            System.out.println(part + " interrupted.");
        }
    }
}

public class FileDownloadSimulation {
    public static void main(String[] args) {
        FileDownload part1 = new FileDownload("Part 1");
        FileDownload part2 = new FileDownload("Part 2");

        part1.start();
        try {
            part1.join();
        } catch (InterruptedException e) {
            e.printStackTrace();
        }

        part2.start();
        try {
            part2.join();
        } catch (InterruptedException e) {
            e.printStackTrace();
        }

        System.out.println("File download completed.");
    }
}
