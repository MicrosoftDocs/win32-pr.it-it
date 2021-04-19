---
description: Specifica la classe di servizio Utilità di pianificazione classi multimediali (MMCSS) per il thread di decodifica.
ms.assetid: 77724879-62e4-439e-9dd0-3642cd7f75ca
title: Proprietà AVDecMmcss (UUIDs. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0092ac516f9600929a9772d044f51e7e375548d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332709"
---
# <a name="avdecmmcss-property"></a>Proprietà AVDecMmcss

Specifica la classe di servizio Utilità di pianificazione classi multimediali (MMCSS) per il thread di decodifica.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVDecMmcssClass**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà è il nome della classe MMCSS.

## <a name="remarks"></a>Commenti

MMCSS consente alle applicazioni di garantire che l'elaborazione con distinzione del tempo abbia l'accesso in ordine di priorità alle risorse della CPU. Funziona elevando i thread registrati a priorità dei thread più elevate, diminuendo periodicamente le priorità per produrre tempo per altri processi.

Il valore consigliato per i decodificatori audio è "audio" e il valore consigliato per i decodificatori video è "Playback".

Se il servizio MMCSS non è disponibile o la classe MMCSS specificata non esiste, l'impostazione della proprietà non ha alcun effetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>UUIDs. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà dell'API codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




