---
title: Proprietà mediaAccessRights di IWMPSettings2
description: La proprietà mediaAccessRights ottiene un valore che indica le autorizzazioni attualmente concesse per l'accesso alla libreria.
ms.assetid: c4289a2c-e343-405d-9bf5-0e97f6617916
keywords:
- Finestra delle proprietà di mediaAccessRights Media Player
- Proprietà di mediaAccessRights Media Player Windows, interfaccia IWMPSettings2
- Interfaccia IWMPSettings2 Windows Media Player, proprietà mediaAccessRights
topic_type:
- apiref
api_name:
- IWMPSettings2.mediaAccessRights
- IWMPSettings2.get_mediaAccessRights
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96cca06b9618767e7748b4b1308ed97860c7c80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324065"
---
# <a name="iwmpsettings2mediaaccessrights-property"></a>Proprietà IWMPSettings2:: mediaAccessRights

La proprietà **mediaAccessRights** ottiene un valore che indica le autorizzazioni attualmente concesse per l'accesso alla libreria.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String mediaAccessRights {get;}
```


```VB

Public ReadOnly Property mediaAccessRights As System.String
```





## <a name="property-value"></a>Valore proprietà

**System. String** che corrisponde a uno dei valori seguenti.



| Valore | Descrizione                      |
|-------|----------------------------------|
| Nessuno  | Solo diritti di accesso agli elementi correnti. |
| lettura  | Solo diritti di accesso in lettura.         |
| completi  | Diritti di accesso in lettura/scrittura.        |



 

## <a name="remarks"></a>Commenti

Una pagina Web deve prima richiedere all'utente l'autorizzazione per la lettura o la scrittura di dati nella libreria. Ciò significa che determinati metodi, proprietà ed eventi saranno inaccessibili dal codice se non sono stati concessi i diritti di accesso appropriati. Per ottenere i diritti di accesso, l'applicazione chiama **IWMPSettings2. Get \_ requestMediaAccessRights**, passando un parametro che specifica il livello di diritti di accesso desiderato.

Le applicazioni in esecuzione nel computer dell'utente dispongono sempre dei diritti di accesso completi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPSettings2 (VB e C#)**](iwmpsettings2--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





