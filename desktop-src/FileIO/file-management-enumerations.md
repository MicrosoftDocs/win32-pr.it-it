---
description: Enumerazioni utilizzate per la gestione dei file.
ms.assetid: 14b1cfff-5e47-4309-8e62-fb5c8da9ce97
title: Enumerazioni di gestione file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7b53d8f53bf9dbe16c15d21171e52ea3dd0015d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968401"
---
# <a name="file-management-enumerations"></a>Enumerazioni di gestione file

Per la gestione dei file vengono utilizzate le enumerazioni seguenti.

## <a name="in-this-section"></a>Contenuto della sezione



| Enumerazione                                                                   | Descrizione                                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Fase di copia COPYFILE2 \_**](/windows/desktop/api/WinBase/ne-winbase-copyfile2_copy_phase)<br/>             | Indica la fase di una copia al momento di un errore.<br/>                                                                                                                                                                           |
| [**\_Azione messaggio \_ COPYFILE2**](/windows/desktop/api/WinBase/ne-winbase-copyfile2_message_action)<br/>     | Restituito dalla funzione di callback [*CopyFile2ProgressRoutine*](/windows/desktop/api/WinBase/nc-winbase-pcopyfile2_progress_routine) per indicare l'azione da intraprendere per l'operazione di copia in sospeso.<br/>                                                             |
| [**\_Tipo di messaggio COPYFILE2 \_**](/windows/desktop/api/WinBase/ne-winbase-copyfile2_message_type)<br/>         | Indica il tipo di messaggio passato nella struttura [**del \_ messaggio COPYFILE2**](/windows/desktop/api/WinBase/ns-winbase-copyfile2_message) alla funzione di callback [*CopyFile2ProgressRoutine*](/windows/desktop/api/WinBase/nc-winbase-pcopyfile2_progress_routine) .<br/>                                       |
| [**\_operazione di controllo CSV \_**](/windows/desktop/api/WinIoCtl/ne-winioctl-csv_control_op)<br/>                         | Specifica il tipo di operazione di controllo CSV da usare con il codice di controllo del [**\_ \_ controllo CSV FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_csv_control) .<br/>                                                                                                       |
| [**\_tipo di ID file \_**](/windows/desktop/api/WinBase/ne-winbase-file_id_type)<br/>                             | Discriminatore per l'Unione nella struttura [**del \_ \_ descrittore dell'ID file**](/windows/desktop/api/WinBase/ns-winbase-file_id_descriptor) .<br/>                                                                                                                                 |
| [**informazioni sul FILE \_ \_ per \_ \_ classe handle**](/windows/win32/api/minwinbase/ne-minwinbase-file_info_by_handle_class)<br/> | Identifica il tipo di informazioni sul file che [**GetFileInformationByHandleEx**](/windows/desktop/api/WinBase/nf-winbase-getfileinformationbyhandleex) deve recuperare o [**SetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-setfileinformationbyhandle) deve impostare.<br/>                |
| [**\_livelli di informazioni Findex \_**](/windows/win32/api/minwinbase/ne-minwinbase-findex_info_levels)<br/>             | Definisce i valori utilizzati con la funzione [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) per specificare il livello di informazioni dei dati restituiti.<br/>                                                                                 |
| [**\_operazioni di ricerca Findex \_**](/windows/win32/api/minwinbase/ne-minwinbase-findex_search_ops)<br/>               | Definisce i valori utilizzati con la funzione [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) per specificare il tipo di filtro da eseguire.<br/>                                                                                           |
| [**OTTENERE \_ i \_ livelli di informazioni FILEEX \_**](/windows/win32/api/minwinbase/ne-minwinbase-get_fileex_info_levels)<br/>        | Definisce i valori utilizzati con le funzioni [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) e [**GetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-getfileattributestransacteda) per specificare il livello di informazioni dei dati restituiti.<br/> |
| [**HINT di priorità \_**](/windows/desktop/api/WinBase/ne-winbase-priority_hint)<br/>                            | Definisce i valori utilizzati con la struttura [**di \_ \_ informazioni del \_ Suggerimento \_ di priorità**](/windows/desktop/api/WinBase/ns-winbase-file_io_priority_hint_info) i/o per specificare l'hint di priorità per un'operazione di I/O di file.<br/>                                                      |
| [**\_livelli di informazioni sui flussi \_**](/windows/desktop/api/fileapi/ne-fileapi-stream_info_levels)<br/>                 | Definisce i valori utilizzati con la funzione [**FindFirstStreamW**](/windows/desktop/api/fileapi/nf-fileapi-findfirststreamw) per specificare il livello di informazioni dei dati restituiti.<br/>                                                                               |



 

 

