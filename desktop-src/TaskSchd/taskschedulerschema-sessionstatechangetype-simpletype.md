---
title: Tipo semplice sessionStateChangeType
description: Definisce i valori per il tipo di Terminal Server modifica dello stato della sessione che è possibile usare per avviare un'attività.
ms.assetid: 56e19ec0-ea6c-4434-ab9d-a1069108920f
keywords:
- Utilità di pianificazione di tipo semplice sessionStateChangeType
topic_type:
- apiref
api_name:
- sessionStateChangeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a77fb563b59ccd8d63d38c6c85f16ff74ac404b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478377"
---
# <a name="sessionstatechangetype-simple-type"></a>Tipo semplice sessionStateChangeType

Definisce i valori per il tipo di Terminal Server modifica dello stato della sessione che è possibile usare per avviare un'attività.

``` syntax
<xs:simpleType name="sessionStateChangeType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="ConsoleConnect"
         />
        <xs:enumeration
            value="ConsoleDisconnect"
         />
        <xs:enumeration
            value="RemoteConnect"
         />
        <xs:enumeration
            value="RemoteDisconnect"
         />
        <xs:enumeration
            value="SessionLock"
         />
        <xs:enumeration
            value="SessionUnlock"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valori di enumerazione

Il tipo semplice **sessionStateChangeType** definisce i valori seguenti.



| Valore             | Descrizione                                                                                                                                                                                       |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ConsoleConnect    | Modifica dello stato di connessione della console Terminal Server. Ad esempio, quando si esegue la connessione a una sessione utente nel computer locale cambiando gli utenti del computer. <br/>                            |
| ConsoleDisconnect | Modifica dello stato di disconnessione della console Terminal Server. Ad esempio, quando si esegue la disconnessione a una sessione utente nel computer locale cambiando gli utenti del computer. <br/>                      |
| RemoteConnect     | Terminal Server modifica dello stato della connessione remota. Ad esempio, quando un utente si connette a una sessione utente utilizzando il programma Connessione Desktop remoto da un computer remoto. <br/>            |
| RemoteDisconnect  | Terminal Server modifica dello stato di disconnessione remota. Ad esempio, quando un utente si disconnette da una sessione utente durante l'utilizzo del programma Connessione Desktop remoto da un computer remoto. <br/> |
| SessionLock       | Modifica dello stato di blocco della sessione Terminal Server. Ad esempio, questa modifica di stato comporta l'esecuzione dell'attività quando il computer è bloccato. <br/>                                                       |
| SessionUnlock     | Modifica dello stato di Terminal Server sessione sbloccata. Ad esempio, questa modifica di stato comporta l'esecuzione dell'attività quando il computer è sbloccato.<br/>                                                    |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





