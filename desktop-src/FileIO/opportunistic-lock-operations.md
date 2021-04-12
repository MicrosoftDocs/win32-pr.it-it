---
description: Se un'applicazione richiede blocchi opportunistici, è necessario aprire tutti i file per cui richiede blocchi per l'input e l'output sovrapposti usando la funzione CreateFile con il flag FILE \_ \_ sovrapposto.
ms.assetid: 1595c03e-9f6d-456c-8164-fafba06bbd79
title: Operazioni di blocco opportunistiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefd9b292747e89f5ebafd94cb8aa0e38833e8cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529137"
---
# <a name="opportunistic-lock-operations"></a>Operazioni di blocco opportunistiche

Se un'applicazione richiede blocchi opportunistici, è necessario aprire tutti i file per cui richiede blocchi per l'input e l'output sovrapposti usando la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con il flag **file \_ \_ sovrapposto** . Dopo l'apertura dei file per un'operazione sovrapposta, è possibile usare la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con uno dei seguenti codici di controllo per lavorare con i blocchi opportunistici di tali file:

<dl>

[**\_ \_ chiusura ACK FSCTL \_ OPBATCH \_ in sospeso**](/windows/win32/api/winioctl/ni-winioctl-fsctl_opbatch_ack_close_pending)  
[**FSCTL \_ blocco opportunistico \_ break \_ ACK \_ No \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_ack_no_2)  
[**\_conferma FSCTL \_ blocco opportunistico \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_acknowledge)  
[**notifica di FSCTL \_ blocco opportunistico \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_notify)  
[**\_ \_ blocco opportunistico batch richieste \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_batch_oplock)  
[**\_ \_ blocco opportunistico filtro richieste \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock)  
[**\_blocco opportunistico richiesta \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock)  
[**FSCTL \_ richiesta \_ blocco opportunistico \_ livello \_ 1**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_1)  
[**FSCTL \_ richiesta \_ blocco opportunistico \_ livello \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_2)  
</dl>

 

 
