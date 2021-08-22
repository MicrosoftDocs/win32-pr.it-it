---
title: WM/WMContentID
description: L'attributo WM/WMContentID contiene un GUID che identifica il contenuto.
ms.assetid: b46d02f4-04f5-430a-b3f7-0f80e03bed2c
keywords:
- Formato multimediale windows WM/WMContentID
topic_type:
- apiref
api_name:
- WM/WMContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef6b1b77bf0305fa0890ea7e85172d77d6e213864c1fc114136bc42e08a8507b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083865"
---
# <a name="wmwmcontentid"></a>WM/WMContentID

**L'attributo WM/WMContentID** contiene un GUID che identifica il contenuto.

## <a name="global-constant"></a>Costante globale

g \_ wszWMWMContentID

## <a name="data-type"></a>Tipo di dati

**GUID DI TIPO WMT \_ \_**

## <a name="remarks"></a>Commenti

Il contenuto viene identificato Windows tecnologie multimediali usando tre valori: **WM/WMCollectionGroupID**, **WM/WMCollectionID** e **WM/WMContentID**. Questi valori identificano il contenuto, la raccolta a cui appartiene e il gruppo a cui appartiene la raccolta. Tutti e tre questi valori vengono popolati Windows Media Player quando vengono recuperati i metadati per il contenuto. È possibile fare in modo che l'applicazione record questi valori e li usi per identificare il contenuto, ma non è consigliabile modificarli se sono presenti.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




