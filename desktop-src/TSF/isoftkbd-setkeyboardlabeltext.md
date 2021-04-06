---
title: Metodo ISoftKbd SetKeyboardLabelText (Softkbdc. h)
description: Il metodo ISoftKbd SetKeyboardLabelText imposta il testo dell'etichetta dal layout per una tastiera soft.
ms.assetid: 86c45c37-fe50-4596-b4c9-960de760a2e0
keywords:
- Framework servizi di testo Metodo SetKeyboardLabelText
- Framework dei servizi di testo del metodo SetKeyboardLabelText, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo SetKeyboardLabelText
topic_type:
- apiref
api_name:
- ISoftKbd.SetKeyboardLabelText
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 862341182b9c97a751ba4a130566d5cf18437c2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742791"
---
# <a name="isoftkbdsetkeyboardlabeltext-method"></a>Metodo ISoftKbd:: SetKeyboardLabelText

Il metodo **ISoftKbd:: SetKeyboardLabelText** imposta il testo dell'etichetta dal layout per una tastiera soft.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetKeyboardLabelText(
  [in] HKL hKl
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hKl* \[ in\]
</dt> <dd>

Handle utilizzato per recuperare il layout installato per la tastiera soft.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                        | Descrizione                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Il metodo è stato eseguito correttamente.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il parametro *hKl* non è valido.<br/> |



 

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

[**ISoftKbd::SetKeyboardLabelTextCombination**](isoftkbd-setkeyboardlabeltextcombination.md)
</dt> </dl>

 

 





