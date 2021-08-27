---
description: Salva il log di grafica nel percorso specificato.
MS-HAID: vspixengine.IPixEngine\_SaveFile\_BSTR\_IFileIOCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Metodo IPixEngine::SaveFile
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A80498F4-C8F5-4AC0-92C5-A90EB2A090B7
api_name:
- IPixEngine.SaveFile
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 737a0de1636fbae4f8beee0be89780b54415e138
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622537"
---
# <a name="span-idvspixengineipixengine_savefile_bstr_ifileiocallback_ptrspanipixenginesavefile-method"></a><span id="vspixengine.ipixengine_savefile_bstr_ifileiocallback_ptr"></span>Metodo IPixEngine::SaveFile

Salva il log di grafica nel percorso specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SaveFile(
   BSTR             FileName,
   IFileIOCallback* pFileIOCallback
);
```

## <a name="parameters"></a>Parametri

*Filename*   
Stringa COM contenente il percorso del log di grafica salvato.

*pFileIOCallback*   
Indirizzo di un functon usato per notificare all'host gli errori di I/O del file durante il salvataggio.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IPixEngine**](/windows/desktop/direct3dtools/ipixengine)

 

 
