---
title: Metodo Initialize ISoftKbd (Softkbdc. h)
description: Il metodo di inizializzazione ISoftKbd Inizializza tutti i campi necessari per una tastiera morbida e genera layout di tastiera soft standard.
ms.assetid: c997864c-2596-4086-8062-cd30f371c38f
keywords:
- Framework dei servizi di testo del metodo Initialize
- Initialize Method Text Services Framework, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo Initialize
topic_type:
- apiref
api_name:
- ISoftKbd.Initialize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6e820becb05d7c474004b4889735f9637e0135a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740207"
---
# <a name="isoftkbdinitialize-method"></a>Metodo ISoftKbd:: Initialize

Il metodo **ISoftKbd:: Initialize** Inizializza tutti i campi necessari per una tastiera morbida e genera layout di tastiera soft standard.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Initialize();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                | Descrizione                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è stato eseguito correttamente.<br/> |



 

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

 

 





