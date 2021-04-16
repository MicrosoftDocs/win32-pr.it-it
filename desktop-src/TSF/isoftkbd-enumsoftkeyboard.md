---
title: Metodo ISoftKbd EnumSoftKeyboard (Softkbdc. h)
description: Il metodo ISoftKbd EnumSoftKeyboard enumera le possibili tastiere soft che supportano la lingua specificata.
ms.assetid: c71f99e5-c4c2-4b09-a58f-d3f4348d0c5d
keywords:
- Framework servizi di testo Metodo EnumSoftKeyboard
- Framework dei servizi di testo del metodo EnumSoftKeyboard, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo EnumSoftKeyboard
topic_type:
- apiref
api_name:
- ISoftKbd.EnumSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ecdb083684163798a68674628a8b1abc2460268
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477999"
---
# <a name="isoftkbdenumsoftkeyboard-method"></a>Metodo ISoftKbd:: EnumSoftKeyboard

Il metodo **ISoftKbd:: EnumSoftKeyboard** enumera le possibili tastiere soft che supportano la lingua specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EnumSoftKeyboard(
  [in]  LANGID langid,
  [out] DWORD  *lpdwKeyboard
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*LangID* \[ in\]
</dt> <dd>

Identificatore della lingua.

</dd> <dt>

*lpdwKeyboard* \[ out\]
</dt> <dd>

Puntatore a un buffer in cui questo metodo recupera gli identificatori delle tastiere flessibili disponibili.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                        | Descrizione                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Il metodo è stato eseguito correttamente.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il parametro *LangID* non è valido.<br/> |



 

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

 

 





