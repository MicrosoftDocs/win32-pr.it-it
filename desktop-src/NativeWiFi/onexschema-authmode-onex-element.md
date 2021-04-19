---
description: Specifica il tipo di credenziali utilizzate per l'autenticazione.
ms.assetid: a56ce888-ec07-4ce8-a540-6d1890cb338d
title: Elemento authMode (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d699b27746226c3eb1550cfd9250e229b40a22e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311676"
---
# <a name="authmode-onex-element"></a>Elemento authMode (OneX)

L'elemento authMode (OneX) specifica il tipo di credenziali usate per l'autenticazione. Nella tabella seguente sono descritti i valori possibili.



| Valore         | Descrizione                                                                                                                                                             |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| machineOrUser | Usare le credenziali del computer o dell'utente. Quando un utente è connesso, le credenziali dell'utente vengono usate per l'autenticazione. Quando nessun utente è connesso, vengono usate le credenziali del computer. |
| computer       | Usare solo le credenziali del computer.                                                                                                                                           |
| utente          | Usare solo le credenziali utente.                                                                                                                                              |
| guest         | Utilizzare solo le credenziali Guest (vuote).                                                                                                                                     |



 

Questo elemento è facoltativo. Quando authMode non viene specificato in un profilo, viene utilizzato un valore di `machineOrUser` .

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento verrà ignorato se è presente in un profilo.

``` syntax
<xs:element name="authMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="machineOrUser"
             />
            <xs:enumeration
                value="machine"
             />
            <xs:enumeration
                value="user"
             />
            <xs:enumeration
                value="guest"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L'elemento **AuthMode** è definito dall'elemento [**Onex**](onexschema-onex-element.md) .

## <a name="remarks"></a>Commenti

Questo parametro può essere impostato dalla riga di comando tramite il comando **netsh wlan set profileparameter** . Per ulteriori informazioni, vedere [comandi Netsh per WLAN (wireless local area network)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**OneX**](onexschema-onex-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**OneX**](onexschema-onex-element.md)
</dt> </dl>

 

 
