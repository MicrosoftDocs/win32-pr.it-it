---
title: WM/WMContentID
description: L'attributo WM/WMContentID contiene un GUID che identifica il contenuto.
ms.assetid: b46d02f4-04f5-430a-b3f7-0f80e03bed2c
keywords:
- Formato di Windows Media WM/WMContentID
topic_type:
- apiref
api_name:
- WM/WMContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ef250e2e2e797ce5ba3c4492c2a3f8b71d30eb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397787"
---
# <a name="wmwmcontentid"></a>WM/WMContentID

L'attributo **WM/WMContentID** contiene un GUID che identifica il contenuto.

## <a name="global-constant"></a>Costante globale

g \_ wszWMWMContentID

## <a name="data-type"></a>Tipo di dati

**\_GUID di tipo WMT \_**

## <a name="remarks"></a>Commenti

Il contenuto viene identificato dalle tecnologie Windows Media usando tre valori: **WM/WMCollectionGroupID**, **WM/WMCollectionID** e **WM/WMContentID**. Questi valori identificano il contenuto, la raccolta a cui appartiene e il gruppo a cui appartiene la raccolta. Tutti e tre questi valori vengono popolati da Windows Media Player quando vengono recuperati i metadati per il contenuto. È possibile fare in modo che l'applicazione registri questi valori e li usi per identificare il contenuto, ma non è necessario modificarli se presenti.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




