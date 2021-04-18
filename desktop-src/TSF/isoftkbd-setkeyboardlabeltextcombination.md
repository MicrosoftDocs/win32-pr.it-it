---
title: Metodo ISoftKbd SetKeyboardLabelTextCombination (Softkbdc. h)
description: Il metodo ISoftKbd SetKeyboardLabelTextCombination imposta una combinazione di etichetta e testo usati per descrivere una tastiera soft.
ms.assetid: fe054eae-1a44-41ad-9a44-bc0b46df7c7b
keywords:
- Framework servizi di testo Metodo SetKeyboardLabelTextCombination
- Framework dei servizi di testo del metodo SetKeyboardLabelTextCombination, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo SetKeyboardLabelTextCombination
topic_type:
- apiref
api_name:
- ISoftKbd.SetKeyboardLabelTextCombination
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f98dad124455625f0da3ada1a717c692437398
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302181"
---
# <a name="isoftkbdsetkeyboardlabeltextcombination-method"></a>Metodo ISoftKbd:: SetKeyboardLabelTextCombination

Il metodo **ISoftKbd:: SetKeyboardLabelTextCombination** imposta una combinazione di etichetta e testo usati per descrivere una tastiera soft.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetKeyboardLabelTextCombination(
  [in] DWORD nModifierCombination
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nModifierCombination* \[ in\]
</dt> <dd>

Combinazione di etichetta e testo usati per descrivere la tastiera soft.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                        | Descrizione                                                 |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Il metodo è stato eseguito correttamente.<br/>                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il parametro *nModifierCombination* non è valido.<br/> |



 

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
</dt> <dt>

[**ISoftKbd::SetKeyboardLabelText**](isoftkbd-setkeyboardlabeltext.md)
</dt> </dl>

 

 





