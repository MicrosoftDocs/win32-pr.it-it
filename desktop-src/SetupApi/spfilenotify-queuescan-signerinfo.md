---
description: La \_ notifica SPFILENOTIFY QUEUESCAN \_ SIGNERINFO viene inviata a una routine di callback da SetupScanFileQueue per ogni nodo nella coda secondaria di copia della coda di file.
ms.assetid: 5b22e8ba-9a18-461b-bad7-b2d76f83d7f3
title: Messaggio SPFILENOTIFY_QUEUESCAN_SIGNERINFO (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e29bf9e9c7e0ab76303d8c2fb21a0109ec60358f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967864"
---
# <a name="spfilenotify_queuescan_signerinfo-message"></a>\_ \_ Messaggio SIGNERINFO QUEUESCAN SPFILENOTIFY

La notifica **SPFILENOTIFY \_ QUEUESCAN \_ SIGNERINFO** viene inviata a una routine di callback da [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) per ogni nodo nella coda secondaria di copia della coda di file. Questo errore si verifica solo se è stata chiamata la funzione **SetupScanFileQueue** specificando il flag SPQ \_ Scan \_ use \_ callback \_ SIGNERINFO. Disponibile a partire da Windows XP.


```C++
SPFILENOTIFY_QUEUESCAN_SIGNERINFO
  Param1 = (PFILEPATHS_SIGNERINFO) Filepaths;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Param1* 
</dt> <dd>

Puntatore a una struttura [**\_ SIGNERINFO filePaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_signerinfo_a) . Il membro di **destinazione** è il nome del file di destinazione nel sistema. Il membro di **origine** è il percorso previsto del file di origine. Il membro **Win32Error** è l'errore di firma. Se la routine di callback restituisce **Win32Error**= = nessun errore, vengono restituite informazioni sulla firma \_ . Il membro **DigitalSigner** è il firmatario digitale. Il membro della **versione** è la versione. **CatalogFile** è il file di catalogo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La routine di callback deve restituire un [codice di errore di sistema](/windows/desktop/Debug/system-error-codes).

Se la routine di callback non restituisce alcun \_ errore, l'analisi della coda continua e restituisce se la routine restituisce un altro codice di errore, l'analisi della coda si interrompe e [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) restituisce **false**.

> [!Note]  
> Questa notifica non viene gestita dalla funzione [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) .

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Setupapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Overview](overview.md)
</dt> <dt>

[Notifications](notifications.md)
</dt> <dt>

[**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

