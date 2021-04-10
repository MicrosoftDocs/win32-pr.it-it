---
description: Attendere l'arresto del motore specificato (chiamata di blocco).
MS-HAID: vspixengine.IServerConnectionCallback\_WaitForShutdown\_IPixEngine\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IServerConnectionCallback:: WaitForShutdown'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B70229D5-3C41-4B50-8336-A1271A9EBE81
api_name:
- IServerConnectionCallback.WaitForShutdown
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d98bd5f398748e6e62a099bcc2be94b5e5f27bc8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125355"
---
# <a name="span-idvspixengineiserverconnectioncallback_waitforshutdown_ipixengine_ptrspaniserverconnectioncallbackwaitforshutdown-method"></a><span id="vspixengine.iserverconnectioncallback_waitforshutdown_ipixengine_ptr"></span>Metodo IServerConnectionCallback:: WaitForShutdown

Attendere l'arresto del motore specificato (chiamata di blocco).

## <a name="syntax"></a>Sintassi


```C++
HRESULT WaitForShutdown(
   IPixEngine * pEngine
);
```

## <a name="parameters"></a>Parametri

*pEngine*   
Motore da arrestare.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IServerConnectionCallback**](/windows/desktop/direct3dtools/iserverconnectioncallback)

 

 
