---
description: Ottiene informazioni sul computer di riproduzione corrente.
MS-HAID: vspixengine.IPixEngine2\_GetPlaybackMachine\_BSTR\_BOOL\_ptr\_BSTR\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPixEngine2:: GetPlaybackMachine'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D6C3C391-F039-4A5A-AA88-87A3624ECAD2
api_name:
- IPixEngine2.GetPlaybackMachine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c572d1a87fb537fd53a7f3e8f8048d1046980b20
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304339"
---
# <a name="span-idvspixengineipixengine2_getplaybackmachine_bstr_bool_ptr_bstr_ptrspanipixengine2getplaybackmachine-method"></a><span id="vspixengine.ipixengine2_getplaybackmachine_bstr_bool_ptr_bstr_ptr"></span>Metodo IPixEngine2:: GetPlaybackMachine

Ottiene informazioni sul computer di riproduzione corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetPlaybackMachine(
   BSTR   logFile,
   BOOL * pUseAuthentication,
   BSTR * pMachine
);
```

## <a name="parameters"></a>Parametri

*logFile*   
Stringa COM contenente il nome del log di grafica associato.

*pUseAuthentication*   
In caso di restituzione, true se la connessione utilizza l'autenticazione di; in caso contrario, false.

*pMachine*   
Al ritorno, stringa COM contenente il nome del computer di riproduzione.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IPixEngine2**](/windows/desktop/direct3dtools/ipixengine2)

 

 
