---
description: Apre un log di grafica.
MS-HAID: vspixengine.IPixEngine\_OpenFile\_BSTR\_BSTR\_INewFramesCallback\_ptr\_IFileIOCallback\_ptr\_LCID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Metodo IPixEngine::OpenFile
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8E0E1336-9FC7-4C32-AF3C-F3BDF39A36D9
api_name:
- IPixEngine.OpenFile
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8f6b2e34258221353baf541ddf76df205472f731
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624348"
---
# <a name="span-idvspixengineipixengine_openfile_bstr_bstr_inewframescallback_ptr_ifileiocallback_ptr_lcidspanipixengineopenfile-method"></a><span id="vspixengine.ipixengine_openfile_bstr_bstr_inewframescallback_ptr_ifileiocallback_ptr_lcid"></span>Metodo IPixEngine::OpenFile

Apre un log di grafica.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OpenFile(
   BSTR                FileName,
   BSTR                registryBoot,
   INewFramesCallback* callbacks,
   IFileIOCallback*    pFileIOCallback,
   LCID                uiLocale
);
```

## <a name="parameters"></a>Parametri

*Filename*   
Stringa COM contenente il nome del log di grafica.

*registryBoot*   
Stringa COM contenente la radice del Registro di sistema. Il motore cerca qui DIA e altre chiavi del Registro di sistema.

*Callback*   
Indirizzo di una funzione utilizzata per notificare all'host che sono stati analizzati nuovi frame.

*pFileIOCallback*   
Indirizzo di una funzione usata per notificare all'host gli errori di I/O del file durante l'analisi.

*uiLocale*   
ID delle impostazioni locali utilizzato per presentare i messaggi di errore in base alle impostazioni locali.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IPixEngine**](/windows/desktop/direct3dtools/ipixengine)

 

 
