---
title: WM/WMCollectionID
description: L'attributo WM/WMCollectionID contiene un GUID che identifica la raccolta.
ms.assetid: 088fe2d7-e2d9-42a3-8deb-1d7948ff7df9
keywords:
- Formato di Windows Media WM/WMCollectionID
topic_type:
- apiref
api_name:
- WM/WMCollectionID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21d2ffe9ca827b19b4ce403b2e2929dea64ae684
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397791"
---
# <a name="wmwmcollectionid"></a>WM/WMCollectionID

L'attributo **WM/WMCollectionID** contiene un GUID che identifica la raccolta.

## <a name="global-constant"></a>Costante globale

g \_ wszWMWMCollectionID

## <a name="data-type"></a>Tipo di dati

**\_GUID di tipo WMT \_**

## <a name="remarks"></a>Commenti

Il contenuto viene identificato dalle tecnologie Windows Media usando tre valori: **WM/WMCollectionGroupID**, **WM/WMCollectionID** e **WM/WMContentID**. Questi valori identificano il contenuto, la raccolta a cui appartiene e il gruppo a cui appartiene la raccolta. Tutti e tre questi valori vengono popolati da Windows Media Player quando vengono recuperati i metadati per il contenuto. È possibile fare in modo che l'applicazione registri questi valori e li usi per identificare il contenuto, ma non è necessario modificarli se presenti.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




