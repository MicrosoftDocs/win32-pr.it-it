---
title: DRM_Flags
description: La \_ Proprietà flag DRM viene utilizzata con contenuto DRM versione 1 solo per specificare i diritti che saranno contenuti nella licenza locale.
ms.assetid: d9a776d3-da22-4111-b1ed-e3607a5576ef
keywords:
- DRM_Flags formato Windows Media
topic_type:
- apiref
api_name:
- DRM_Flags
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4f2f8eb2baa401f1bc8519da5ca555a1fe428ee
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103956185"
---
# <a name="drm_flags"></a>\_Flag DRM

La **proprietà \_ flag DRM** viene utilizzata con contenuto DRM versione 1 solo per specificare i diritti che saranno contenuti nella licenza locale. I diritti vengono specificati con i valori definiti dal tipo di enumerazione **\_ dei diritti WMT** . È possibile selezionare più di un valore unendoli con **l'operatore OR** bit per bit.

## <a name="global-constant"></a>Costante globale

\_flag g wszWMDRM \_

## <a name="data-type"></a>Tipo di dati

**WMT \_ tipo \_ DWORD**

## <a name="remarks"></a>Commenti

Quando si accede all'interfaccia **IWMHeaderInfo3** dell'oggetto writer, è possibile aggiungere o modificare questo valore. In altri oggetti (editor di metadati, lettore e lettore sincrono), questo valore è di sola lettura. Usare [**IWMHeaderInfo:: SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) per impostare questa proprietà quando si crea contenuto DRM versione 1.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà DRM**](drm-properties.md)
</dt> </dl>

 

 




