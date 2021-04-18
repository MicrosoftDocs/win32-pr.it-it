---
title: Metodo IWMPSettings2 requestMediaAccessRights
description: Il metodo requestMediaAccessRights richiede un livello specificato di accesso alla libreria. | Metodo IWMPSettings2 requestMediaAccessRights
ms.assetid: ea33852c-d1e0-45cf-8954-2a1e2fe51910
keywords:
- Metodo requestMediaAccessRights Windows Media Player
- Metodo requestMediaAccessRights Windows Media Player, interfaccia IWMPSettings2
- Interfaccia IWMPSettings2 Windows Media Player, metodo requestMediaAccessRights
topic_type:
- apiref
api_name:
- IWMPSettings2.requestMediaAccessRights
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c609afffc1d9b228d908d905e0eb1a6ef8741032
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328195"
---
# <a name="iwmpsettings2requestmediaaccessrights-method"></a>Metodo IWMPSettings2:: requestMediaAccessRights

Il metodo **requestMediaAccessRights** richiede un livello specificato di accesso alla libreria.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Boolean requestMediaAccessRights(
  System.String bstrDesiredAccess
);
```


```VB

Public Function requestMediaAccessRights( _
  ByVal bstrDesiredAccess As System.String _
) As System.Boolean
Implements IWMPSettings2.requestMediaAccessRights
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrDesiredAccess* \[ in\]
</dt> <dd>

**System. String** che corrisponde a uno dei valori seguenti.



| Valore | Descrizione                      |
|-------|----------------------------------|
| Nessuno  | Solo diritti di accesso agli elementi correnti. |
| lettura  | Solo diritti di accesso in lettura.         |
| completi  | Diritti di accesso in lettura/scrittura.        |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**System. Boolean** che indica se sono stati concessi i diritti di accesso richiesti.

## <a name="remarks"></a>Commenti

Una pagina Web deve prima richiedere all'utente l'autorizzazione per la lettura o la scrittura di dati nella libreria. La chiamata di questo metodo richiede all'utente una finestra di dialogo che richiede il livello di autorizzazione specificato. Ciò significa che determinati metodi, proprietà ed eventi saranno inaccessibili dal codice se non sono stati concessi i diritti di accesso appropriati. Il livello dei diritti di accesso corrente può essere recuperato tramite **IWMPSettings2. mediaAccessRights**.

Per le applicazioni in esecuzione nel computer dell'utente non è necessario usare questo metodo.

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

[**IWMPSettings2. mediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





