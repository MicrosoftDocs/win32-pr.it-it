---
description: Carica una trama da un file e invia una notifica all'host in modo asincrono al completamento.
MS-HAID: vspixengine.IPixEngine5\_LoadTextureFromFileAsync\_BSTR\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Metodo IPixEngine5::LoadTextureFromFileAsync
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: DF10C209-B6B5-4692-81D7-7FD59CE49F56
api_name:
- IPixEngine5.LoadTextureFromFileAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d6df20bd48b32cea76192e114f24ff669765b75d
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122629730"
---
# <a name="span-idvspixengineipixengine5_loadtexturefromfileasync_bstr_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5loadtexturefromfileasync-method"></a><span id="vspixengine.ipixengine5_loadtexturefromfileasync_bstr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>Metodo IPixEngine5::LoadTextureFromFileAsync

Carica una trama da un file e invia una notifica all'host in modo asincrono al completamento.

## <a name="syntax"></a>Sintassi


```C++
HRESULT LoadTextureFromFileAsync(
   BSTR                  fileName,
   BSTR                  histogramDataFileName,
   IPixEngine5Callbacks* callbacks,
   DWORD                 requestCookie,
   DWORD                 progressIntervalMsecs
);
```

## <a name="parameters"></a>Parametri

*Filename*   
Stringa COM contenente il nome del file di trama.

*histogramDataFileName*   
Stringa COM contenente il nome del file di dati dell'istogramma associato alla trama.

*Callback*   
Indirizzo di un oggetto che fornisce l'interfaccia di callback IPixEngine5.

*requestCookie*   
Cookie che soddisfa in modo univoco la richiesta e può essere usato per segnalare l'annullamento.

*progressIntervalMsecs*   
Non usato.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IPixEngine5**](/windows/desktop/direct3dtools/ipixengine5)

 

 
