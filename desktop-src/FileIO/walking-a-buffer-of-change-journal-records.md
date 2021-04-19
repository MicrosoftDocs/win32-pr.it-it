---
description: Come restituire i record del journal delle modifiche che soddisfano i criteri specificati.
ms.assetid: 8946adb5-da47-4711-8800-86f323081c4c
title: Analisi di un buffer di record del journal delle modifiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9384316e38c23951849006efc259268a7bdf33df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313872"
---
# <a name="walking-a-buffer-of-change-journal-records"></a><span data-ttu-id="cb467-103">Analisi di un buffer di record del journal delle modifiche</span><span class="sxs-lookup"><span data-stu-id="cb467-103">Walking a Buffer of Change Journal Records</span></span>

<span data-ttu-id="cb467-104">I codici di controllo che restituiscono i record del journal delle modifiche USN (Update Sequence Number), [**FSCTL \_ Read \_ USN \_ Journal**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) e [**FSCTL \_ enum \_ USN \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data), restituiscono dati simili nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="cb467-104">The control codes that return update sequence number (USN) change journal records, [**FSCTL\_READ\_USN\_JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) and [**FSCTL\_ENUM\_USN\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data), return similar data in the output buffer.</span></span> <span data-ttu-id="cb467-105">Entrambi restituiscono un USN seguito da zero o più record del journal delle modifiche, ognuno in una struttura di record [**USN \_ \_ v2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) o [**\_ record USN \_ v3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) .</span><span class="sxs-lookup"><span data-stu-id="cb467-105">Both return a USN followed by zero or more change journal records, each in a [**USN\_RECORD\_V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) or [**USN\_RECORD\_V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) structure.</span></span>

<span data-ttu-id="cb467-106">Il volume di destinazione per le operazioni USN deve essere ReFS o NTFS 3,0 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="cb467-106">The target volume for USN operations must be ReFS or NTFS 3.0 or later.</span></span> <span data-ttu-id="cb467-107">Per ottenere la versione NTFS di un volume, aprire un prompt dei comandi con diritti di accesso di amministratore ed eseguire il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="cb467-107">To obtain the NTFS version of a volume, open a command prompt with Administrator access rights and execute the following command:</span></span>

<span data-ttu-id="cb467-108">**FSUtil.exe FSInfo NTFSInfo** *X \* \* *:**</span><span class="sxs-lookup"><span data-stu-id="cb467-108">**FSUtil.exe FSInfo NTFSInfo** *X\*\*\*:*\*</span></span>

<span data-ttu-id="cb467-109">dove *X* è la lettera di unità del volume.</span><span class="sxs-lookup"><span data-stu-id="cb467-109">where *X* is the drive letter of the volume.</span></span>

<span data-ttu-id="cb467-110">Nell'elenco seguente vengono illustrate le modalità di ottenimento dei record del journal delle modifiche:</span><span class="sxs-lookup"><span data-stu-id="cb467-110">The following list identifies ways to get change journal records:</span></span>

-   <span data-ttu-id="cb467-111">Usare [**\_ \_ \_ i dati USN dell'enumerazione FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data) per ottenere un elenco (enumerazione) di tutti i record del journal delle modifiche tra due USNs.</span><span class="sxs-lookup"><span data-stu-id="cb467-111">Use [**FSCTL\_ENUM\_USN\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data) to get a listing (enumeration) of all change journal records between two USNs.</span></span>
-   <span data-ttu-id="cb467-112">Usare [**FSCTL \_ Read \_ USN \_ Journal**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) per essere più selettivi, ad esempio la selezione di motivi specifici per le modifiche o la restituzione di un file chiuso.</span><span class="sxs-lookup"><span data-stu-id="cb467-112">Use [**FSCTL\_READ\_USN\_JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) to be more selective, such as selecting specific reasons for changes or returning when a file is closed.</span></span>

> [!Note]  
> <span data-ttu-id="cb467-113">Entrambe queste operazioni restituiscono solo il subset di record del journal delle modifiche che soddisfano i criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="cb467-113">Both of these operations return only the subset of change journal records that meet the specified criteria.</span></span>

 

<span data-ttu-id="cb467-114">L'USN restituito come primo elemento nel buffer di output è l'USN del numero di record successivo da recuperare.</span><span class="sxs-lookup"><span data-stu-id="cb467-114">The USN returned as the first item in the output buffer is the USN of the next record number to be retrieved.</span></span> <span data-ttu-id="cb467-115">Utilizzare questo valore per continuare a leggere i record dal limite finale in avanti.</span><span class="sxs-lookup"><span data-stu-id="cb467-115">Use this value to continue reading records from the end boundary forward.</span></span>

<span data-ttu-id="cb467-116">Il membro **filename** del [**\_ record USN \_ v2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) o [**\_ record USN \_ v3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) contiene il nome del file a cui si applica il record in questione.</span><span class="sxs-lookup"><span data-stu-id="cb467-116">The **FileName** member of [**USN\_RECORD\_V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) or [**USN\_RECORD\_V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) contains the name of the file to which the record in question applies.</span></span> <span data-ttu-id="cb467-117">Il nome del file varia di lunghezza, quindi il **\_ record USN \_ v2** e il **\_ record USN \_ v3** sono strutture a lunghezza variabile.</span><span class="sxs-lookup"><span data-stu-id="cb467-117">The file name varies in length, so **USN\_RECORD\_V2** and **USN\_RECORD\_V3** are variable length structures.</span></span> <span data-ttu-id="cb467-118">Il primo membro, **RecordLength**, è la lunghezza della struttura, incluso il nome del file, in byte.</span><span class="sxs-lookup"><span data-stu-id="cb467-118">Their first member, **RecordLength**, is the length of the structure (including the file name), in bytes.</span></span>

<span data-ttu-id="cb467-119">Quando si lavora con il membro **filename** delle strutture del [**\_ record USN \_ v2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) e del [**\_ record USN \_ v3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) , non presupporre che il nome del file contenga un \\ delimitatore ' 0' finale.</span><span class="sxs-lookup"><span data-stu-id="cb467-119">When you work with the **FileName** member of [**USN\_RECORD\_V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) and [**USN\_RECORD\_V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) structures, do not assume that the file name contains a trailing '\\0' delimiter.</span></span> <span data-ttu-id="cb467-120">Per determinare la lunghezza del nome file, usare il membro **FileNameLength** .</span><span class="sxs-lookup"><span data-stu-id="cb467-120">To determine the length of the file name, use the **FileNameLength** member.</span></span>

<span data-ttu-id="cb467-121">Nell'esempio seguente viene chiamato [**FSCTL \_ Read \_ USN \_ Journal**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) e viene analizzato il buffer dei record del journal delle modifiche restituiti dall'operazione.</span><span class="sxs-lookup"><span data-stu-id="cb467-121">The following example calls [**FSCTL\_READ\_USN\_JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) and walks the buffer of change journal records that the operation returns.</span></span>


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



<span data-ttu-id="cb467-122">La dimensione in byte di qualsiasi record specificato da un [**\_ record USN \_ v2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) o dalla struttura [**\_ record USN \_ v3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) è al massimo `((MaxComponentLength - 1) * Width) + Size` dove *MaxComponentLength* è la lunghezza massima in caratteri del nome del file di record.</span><span class="sxs-lookup"><span data-stu-id="cb467-122">The size in bytes of any record specified by a [**USN\_RECORD\_V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) or [**USN\_RECORD\_V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) structure is at most `((MaxComponentLength - 1) * Width) + Size` where *MaxComponentLength* is the maximum length in characters of the record file name.</span></span> <span data-ttu-id="cb467-123">La larghezza è la dimensione di un carattere wide e la dimensione *corrisponde alla* dimensione della struttura.</span><span class="sxs-lookup"><span data-stu-id="cb467-123">The width is the size of a wide character, and the *Size* is the size of the structure.</span></span>

<span data-ttu-id="cb467-124">Per ottenere la lunghezza massima, chiamare la funzione [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) ed esaminare il valore a cui punta il parametro *lpMaximumComponentLength* .</span><span class="sxs-lookup"><span data-stu-id="cb467-124">To obtain the maximum length, call the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function and examine the value pointed to by the *lpMaximumComponentLength* parameter.</span></span> <span data-ttu-id="cb467-125">Sottrarre un oggetto da *MaxComponentLength* per tenere conto del fatto che la definizione del [**\_ record USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) e del [**\_ record USN \_ v3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) include un carattere del nome file.</span><span class="sxs-lookup"><span data-stu-id="cb467-125">Subtract one from *MaxComponentLength* to account for the fact that the definition of [**USN\_RECORD**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) and [**USN\_RECORD\_V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) includes one character of the file name.</span></span>

<span data-ttu-id="cb467-126">Nel linguaggio di programmazione C, la dimensione massima possibile per i record è la seguente:</span><span class="sxs-lookup"><span data-stu-id="cb467-126">In the C programming language, the largest possible record size is the following:</span></span>

`(MaxComponentLength - 1) * sizeof(WCHAR) + sizeof(USN_RECORD)`

 

 
