---
title: Tipo semplice sessionStateChangeType
description: Definisce i valori per il tipo di modifica dello stato sessione di Terminal Server che è possibile usare per attivare l'avvio di un'attività.
ms.assetid: 56e19ec0-ea6c-4434-ab9d-a1069108920f
keywords:
- Tipo semplice sessionStateChangeType Utilità di pianificazione
topic_type:
- apiref
api_name:
- sessionStateChangeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a67334b2e8d51404a0e5e78a7d2b3e49908cd1c6ce74f499e66272d2db9be910
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099811"
---
# <a name="sessionstatechangetype-simple-type"></a>Tipo semplice sessionStateChangeType

Definisce i valori per il tipo di modifica dello stato sessione di Terminal Server che è possibile usare per attivare l'avvio di un'attività.

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

Il **tipo semplice sessionStateChangeType** definisce i valori seguenti.



| Valore             | Descrizione                                                                                                                                                                                       |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ConsoleConnetti    | Modifica dello stato della connessione della console di Terminal Server. Ad esempio, quando ci si connette a una sessione utente nel computer locale passando gli utenti nel computer. <br/>                            |
| ConsoleDisconnect | Modifica dello stato di disconnessione della console di Terminal Server. Ad esempio, quando si esegue la disconnessione a una sessione utente nel computer locale passando gli utenti nel computer. <br/>                      |
| Connessione remota     | Modifica dello stato della connessione remota di Terminal Server. Ad esempio, quando un utente si connette a una sessione utente usando il Connessione Desktop remoto da un computer remoto. <br/>            |
| RemoteDisconnect  | Modifica dello stato di disconnessione remota di Terminal Server. Ad esempio, quando un utente si disconnette da una sessione utente durante l'Connessione Desktop remoto programma da un computer remoto. <br/> |
| SessionLock       | Modifica dello stato di blocco della sessione di Terminal Server. Ad esempio, questa modifica dello stato determina l'esecuzione dell'attività quando il computer è bloccato. <br/>                                                       |
| SessionUnlock     | Modifica dello stato di sblocco della sessione di Terminal Server. Ad esempio, questa modifica dello stato determina l'esecuzione dell'attività quando il computer viene sbloccato.<br/>                                                    |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 





