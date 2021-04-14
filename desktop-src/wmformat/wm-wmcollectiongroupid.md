---
title: WM/WMCollectionGroupID
description: L'attributo WM/WMCollectionGroupID contiene un GUID che identifica il gruppo di raccolta.
ms.assetid: 5cfa1747-ce3b-4e8d-bcce-84fb719123e8
keywords:
- Formato di Windows Media WM/WMCollectionGroupID
topic_type:
- apiref
api_name:
- WM/WMCollectionGroupID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 652007933669db4ed7977474858c7089ca0d577f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397790"
---
# <a name="wmwmcollectiongroupid"></a>WM/WMCollectionGroupID

L'attributo **WM/WMCollectionGroupID** contiene un GUID che identifica il gruppo di raccolta.

## <a name="global-constant"></a>Costante globale

g \_ wszWMWMCollectionGroupID

## <a name="data-type"></a>Tipo di dati

**\_GUID di tipo WMT \_**

## <a name="remarks"></a>Commenti

Il contenuto viene identificato dalle tecnologie Windows Media usando tre valori: **WM/WMCollectionGroupID**, **WM/WMCollectionID** e **WM/WMContentID**. Questi valori identificano il contenuto, la raccolta a cui appartiene e il gruppo a cui appartiene la raccolta. Tutti e tre questi valori vengono popolati da Windows Media Player quando vengono recuperati i metadati per il contenuto. È possibile fare in modo che l'applicazione registri questi valori e li usi per identificare il contenuto, ma non è necessario modificarli se presenti.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




