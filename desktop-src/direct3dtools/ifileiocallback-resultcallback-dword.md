---
description: Funzione di callback utilizzata per notificare l'host degli errori durante l'acquisizione o la riproduzione.
MS-HAID: vspixengine.IFileIOCallback\_ResultCallback\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IFileIOCallback:: ResultCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E4418A63-47C6-4F12-94FA-0F1B5465FE84
api_name:
- IFileIOCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 751c4d0b57165e148002218ae2151aaba69e48f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124620"
---
# <a name="span-idvspixengineifileiocallback_resultcallback_dwordspanifileiocallbackresultcallback-method"></a><span id="vspixengine.ifileiocallback_resultcallback_dword"></span>Metodo IFileIOCallback:: ResultCallback

Funzione di callback utilizzata per notificare l'host degli errori durante l'acquisizione o la riproduzione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ResultCallback(
   DWORD resultState
);
```

## <a name="parameters"></a>Parametri

*resultState*   
Indica il tipo di errore rilevato.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IFileIOCallback**](/windows/desktop/direct3dtools/ifileiocallback)

 

 
