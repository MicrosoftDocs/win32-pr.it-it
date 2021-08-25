---
description: Come restituire i record del journal delle modifiche che soddisfano i criteri specificati.
ms.assetid: 8946adb5-da47-4711-8800-86f323081c4c
title: Memorizzazione di un buffer di record del journal delle modifiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9242d671cedfb5c9ef2b5fa836e29c455d09a9e1287b1ed035712f49c6c7d627
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830151"
---
# <a name="walking-a-buffer-of-change-journal-records"></a>Memorizzazione di un buffer di record del journal delle modifiche

I codici di controllo che restituiscono record del journal delle modifiche USN (Update Sequence Number), [**FSCTL \_ READ \_ USN \_ JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) e [**FSCTL \_ ENUM \_ USN \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data)restituiscono dati simili nel buffer di output. Entrambi restituiscono un USN seguito da zero o più record del journal delle modifiche, ognuno in una struttura [**USN \_ RECORD \_ V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) [**o USN RECORD \_ \_ V3.**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3)

Il volume di destinazione per le operazioni USN deve essere ReFS o NTFS 3.0 o versione successiva. Per ottenere la versione NTFS di un volume, aprire un prompt dei comandi con diritti di accesso amministratore ed eseguire il comando seguente:

**FSUtil.exe FSInfo NTFSInfo** *X***:**

dove *X* è la lettera di unità del volume.

L'elenco seguente identifica i modi per ottenere i record del journal delle modifiche:

-   Usare [**FSCTL \_ ENUM \_ USN \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data) per ottenere un elenco (enumerazione) di tutti i record del journal delle modifiche tra due USN.
-   Usare [**FSCTL \_ READ \_ USN \_ JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) per essere più selettivo, ad esempio per la selezione di motivi specifici per le modifiche o la restituzione quando un file viene chiuso.

> [!Note]  
> Entrambe queste operazioni restituiscono solo il subset di record del journal delle modifiche che soddisfano i criteri specificati.

 

L'USN restituito come primo elemento nel buffer di output è l'USN del numero di record successivo da recuperare. Usare questo valore per continuare a leggere i record dal limite finale in avanti.

Il **membro FileName** di [**USN RECORD \_ \_ V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) o [**USN RECORD \_ \_ V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) contiene il nome del file a cui si applica il record in questione. Il nome del file varia in lunghezza, quindi **USN \_ RECORD \_ V2** e **USN \_ RECORD \_ V3** sono strutture a lunghezza variabile. Il primo membro, **RecordLength**, è la lunghezza della struttura (incluso il nome del file), in byte.

Quando si usa il membro **FileName** delle strutture [**USN \_ RECORD \_ V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) e [**USN \_ RECORD \_ V3,**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) non presupporre che il nome file contenga un delimitatore \\ "0" finale. Per determinare la lunghezza del nome file, usare il **membro FileNameLength.**

L'esempio seguente chiama [**FSCTL \_ READ \_ USN \_ JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) e illustra il buffer dei record del journal delle modifiche restituiti dall'operazione.


```C++
#include <Windows.h>
#include <WinIoCtl.h>
#include <stdio.h>

#define BUF_LEN 4096

void main()
{
   HANDLE hVol;
   CHAR Buffer[BUF_LEN];

   USN_JOURNAL_DATA JournalData;
   READ_USN_JOURNAL_DATA ReadData = {0, 0xFFFFFFFF, FALSE, 0, 0};
   PUSN_RECORD UsnRecord;  

   DWORD dwBytes;
   DWORD dwRetBytes;
   int I;

   hVol = CreateFile( TEXT("\\\\.\\c:"), 
               GENERIC_READ | GENERIC_WRITE, 
               FILE_SHARE_READ | FILE_SHARE_WRITE,
               NULL,
               OPEN_EXISTING,
               0,
               NULL);

   if( hVol == INVALID_HANDLE_VALUE )
   {
      printf("CreateFile failed (%d)\n", GetLastError());
      return;
   }

   if( !DeviceIoControl( hVol, 
          FSCTL_QUERY_USN_JOURNAL, 
          NULL,
          0,
          &JournalData,
          sizeof(JournalData),
          &dwBytes,
          NULL) )
   {
      printf( "Query journal failed (%d)\n", GetLastError());
      return;
   }

   ReadData.UsnJournalID = JournalData.UsnJournalID;

   printf( "Journal ID: %I64x\n", JournalData.UsnJournalID );
   printf( "FirstUsn: %I64x\n\n", JournalData.FirstUsn );

   for(I=0; I<=10; I++)
   {
      memset( Buffer, 0, BUF_LEN );

      if( !DeviceIoControl( hVol, 
            FSCTL_READ_USN_JOURNAL, 
            &ReadData,
            sizeof(ReadData),
            &Buffer,
            BUF_LEN,
            &dwBytes,
            NULL) )
      {
         printf( "Read journal failed (%d)\n", GetLastError());
         return;
      }

      dwRetBytes = dwBytes - sizeof(USN);

      // Find the first record
      UsnRecord = (PUSN_RECORD)(((PUCHAR)Buffer) + sizeof(USN));  

      printf( "****************************************\n");

      // This loop could go on for a long time, given the current buffer size.
      while( dwRetBytes > 0 )
      {
         printf( "USN: %I64x\n", UsnRecord->Usn );
         printf("File name: %.*S\n", 
                  UsnRecord->FileNameLength/2, 
                  UsnRecord->FileName );
         printf( "Reason: %x\n", UsnRecord->Reason );
         printf( "\n" );

         dwRetBytes -= UsnRecord->RecordLength;

         // Find the next record
         UsnRecord = (PUSN_RECORD)(((PCHAR)UsnRecord) + 
                  UsnRecord->RecordLength); 
      }
      // Update starting USN for next call
      ReadData.StartUsn = *(USN *)&Buffer; 
   }

   CloseHandle(hVol);

}
```



La dimensione in byte di qualsiasi record specificato da una struttura [**USN \_ RECORD \_ V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) o [**USN \_ RECORD \_ V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) è al massimo dove `((MaxComponentLength - 1) * Width) + Size` *MaxComponentLength* è la lunghezza massima in caratteri del nome del file di record. La larghezza è la dimensione di un carattere wide e *size* è la dimensione della struttura .

Per ottenere la lunghezza massima, chiamare la [**funzione GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) ed esaminare il valore a cui punta *il parametro lpMaximumComponentLength.* Sottrarre uno da *MaxComponentLength* per fare in modo che la definizione di [**USN \_ RECORD**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) e [**USN \_ RECORD \_ V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) includa un carattere del nome file.

Nel linguaggio di programmazione C le dimensioni massime possibili per i record sono le seguenti:

`(MaxComponentLength - 1) * sizeof(WCHAR) + sizeof(USN_RECORD)`

 

 
