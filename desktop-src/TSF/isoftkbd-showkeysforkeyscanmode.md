---
title: Metodo ISoftKbd ShowKeysForKeyScanMode (Softkbdc.h)
description: Il metodo ISoftKbd ShowKeysForKeyScanMode visualizza i tasti usati per la modalità di analisi dei tasti per una tastiera soft.
ms.assetid: bfa76e5b-6f6e-470a-ba3a-7ecff9f67f7b
keywords:
- Metodo ShowKeysForKeyScanMode Framework servizi di testo
- Metodo ShowKeysForKeyScanMode Framework servizi di testo, interfaccia ISoftKbd
- Interfaccia ISoftKbd Framework servizi di testo metodo ShowKeysForKeyScanMode
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
ms.openlocfilehash: 844c9f39529e1a66437c83672acc8b2d3ad2a3e3ff3a1ad31c4d9bd97248d010
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118877273"
---
# <a name="isoftkbdshowkeysforkeyscanmode-method"></a>Metodo ISoftKbd::ShowKeysForKeyScanMode

Il **metodo ISoftKbd::ShowKeysForKeyScanMode** visualizza i tasti usati per la modalità di analisi dei tasti per una tastiera soft.

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

*lpKeyID* \[ Pollici\]
</dt> <dd>

Puntatore a una matrice di elementi KEYID che indica gli identificatori delle chiavi da visualizzare.

</dd> <dt>

*iKeyNum* \[ Pollici\]
</dt> <dd>

Numero di chiavi da visualizzare.

</dd> <dt>

*fHighL* \[ Pollici\]
</dt> <dd>

TRUE se il metodo deve evidenziare le chiavi e **FALSE in caso contrario.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                        | Descrizione                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Il metodo è stato eseguito correttamente.<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Uno dei parametri non è valido.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Componente ridistribuibile<br/>          | TSF 1.0 in Windows 2000 Professional<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Softkbdc.h</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Softkbd.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> </dl>

 

 





