---
title: WM/WMCollectionGroupID
description: L'attributo WM/WMCollectionGroupID contiene un GUID che identifica il gruppo di raccolta.
ms.assetid: 5cfa1747-ce3b-4e8d-bcce-84fb719123e8
keywords:
- WM/WMCollectionGroupID windows Media Format
topic_type:
- apiref
api_name:
- WM/WMCollectionGroupID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12b9d89724751e778eb9545b6c743dbfbcf077b860a8d85c5ab9297680deb930
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118698235"
---
# <a name="wmwmcollectiongroupid"></a>WM/WMCollectionGroupID

**L'attributo WM/WMCollectionGroupID** contiene un GUID che identifica il gruppo di raccolta.

## <a name="global-constant"></a>Costante globale

g \_ wszWMWMCollectionGroupID

## <a name="data-type"></a>Tipo di dati

**GUID DEL \_ TIPO \_ WMT**

## <a name="remarks"></a>Commenti

Il contenuto viene identificato Windows tecnologie multimediali usando tre valori: **WM/WMCollectionGroupID**, **WM/WMCollectionID** e **WM/WMContentID**. Questi valori identificano il contenuto, la raccolta a cui appartiene e il gruppo a cui appartiene la raccolta. Tutti e tre questi valori vengono popolati Windows Media Player quando vengono recuperati i metadati per il contenuto. È possibile fare in modo che l'applicazione registri questi valori e li usi per identificare il contenuto, ma non è consigliabile modificarli se sono presenti.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




