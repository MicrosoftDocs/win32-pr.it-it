---
title: Metodo ISoftKbd ShowKeysForKeyScanMode (Softkbdc. h)
description: Il metodo ISoftKbd ShowKeysForKeyScanMode Visualizza le chiavi usate per la modalità di analisi della chiave per una tastiera soft.
ms.assetid: bfa76e5b-6f6e-470a-ba3a-7ecff9f67f7b
keywords:
- Framework servizi di testo Metodo ShowKeysForKeyScanMode
- Framework dei servizi di testo del metodo ShowKeysForKeyScanMode, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo ShowKeysForKeyScanMode
topic_type:
- apiref
api_name:
- ISoftKbd.ShowKeysForKeyScanMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7c46fbfc103c0ba40294e4c149d5fd427296765
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478203"
---
# <a name="isoftkbdshowkeysforkeyscanmode-method"></a>Metodo ISoftKbd:: ShowKeysForKeyScanMode

Il metodo **ISoftKbd:: ShowKeysForKeyScanMode** Visualizza le chiavi usate per la modalità di analisi della chiave per una tastiera soft.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ShowKeysForKeyScanMode(
  [in] KEYID *lpKeyID,
  [in] INT   iKeyNum,
  [in] BOOL  fHighL
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpKeyID* \[ in\]
</dt> <dd>

Puntatore a una matrice di elementi KEYID che indica gli identificatori delle chiavi da visualizzare.

</dd> <dt>

*iKeyNum* \[ in\]
</dt> <dd>

Numero di chiavi da visualizzare.

</dd> <dt>

*fHighL* \[ in\]
</dt> <dd>

TRUE se il metodo deve evidenziare le chiavi e **false** in caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                        | Descrizione                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Il metodo è stato eseguito correttamente.<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Uno dei parametri non è valido.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Componente ridistribuibile<br/>          | TSF 1,0 su Windows 2000 Professional<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> </dl>

 

 





