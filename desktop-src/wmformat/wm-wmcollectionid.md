---
title: WM/WMCollectionID
description: L'attributo WM/WMCollectionID contiene un GUID che identifica la raccolta.
ms.assetid: 088fe2d7-e2d9-42a3-8deb-1d7948ff7df9
keywords:
- WM/WMCollectionID windows Media Format
topic_type:
- apiref
api_name:
- WM/WMCollectionID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9ad7e22c6769d459dc3d99b964a2df8e4dc562c709a231163d05a1b6b0be911
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928831"
---
# <a name="wmwmcollectionid"></a>WM/WMCollectionID

**L'attributo WM/WMCollectionID** contiene un GUID che identifica la raccolta.

## <a name="global-constant"></a>Costante globale

g \_ wszWMWMCollectionID

## <a name="data-type"></a>Tipo di dati

**GUID DEL \_ TIPO \_ WMT**

## <a name="remarks"></a>Commenti

Il contenuto viene identificato Windows tecnologie multimediali usando tre valori: **WM/WMCollectionGroupID**, **WM/WMCollectionID** e **WM/WMContentID**. Questi valori identificano il contenuto, la raccolta a cui appartiene e il gruppo a cui appartiene la raccolta. Tutti e tre questi valori vengono popolati Windows Media Player quando vengono recuperati i metadati per il contenuto. È possibile fare in modo che l'applicazione registri questi valori e li usi per identificare il contenuto, ma non è consigliabile modificarli se sono presenti.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




