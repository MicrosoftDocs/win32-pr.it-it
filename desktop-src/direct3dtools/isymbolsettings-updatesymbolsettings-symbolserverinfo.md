---
description: Un Request to Send i percorsi dei simboli di debug al motore locale (non remoto).
MS-HAID: vspixengine.ISymbolSettings\_UpdateSymbolSettings\_SymbolServerInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo ISymbolSettings:: UpdateSymbolSettings'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E48E509F-8C33-49D6-B799-B16F70C1AA64
api_name:
- ISymbolSettings.UpdateSymbolSettings
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4c60ceacbf8d11f951896979862dad6520c32837
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303834"
---
# <a name="span-idvspixengineisymbolsettings_updatesymbolsettings_symbolserverinfospanisymbolsettingsupdatesymbolsettings-method"></a><span id="vspixengine.isymbolsettings_updatesymbolsettings_symbolserverinfo"></span>Metodo ISymbolSettings:: UpdateSymbolSettings

Un Request to Send i percorsi dei simboli di debug al motore locale (non remoto).

## <a name="syntax"></a>Sintassi


```C++
HRESULT UpdateSymbolSettings(
   SymbolServerInfo symbolServerInfo
);
```

## <a name="parameters"></a>Parametri

*symbolServerInfo*   
Informazioni sul percorso del server di simboli di debug.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**ISymbolSettings**](/windows/desktop/direct3dtools/isymbolsettings)

 

 
