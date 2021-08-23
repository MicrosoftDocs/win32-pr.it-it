---
title: DRM_Flags
description: La proprietà Flag DRM viene usata con il contenuto DRM versione 1 solo per specificare i diritti che \_ saranno contenuti nella licenza locale.
ms.assetid: d9a776d3-da22-4111-b1ed-e3607a5576ef
keywords:
- DRM_Flags windows Media Format
topic_type:
- apiref
api_name:
- DRM_Flags
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adf4f1b2065eb1b251f0c555f8c33e424e43aefd04377ed894edb90c121aacb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086012"
---
# <a name="drm_flags"></a>Flag \_ DRM

La **proprietà \_ Flag DRM** viene usata con il contenuto DRM versione 1 solo per specificare i diritti che saranno contenuti nella licenza locale. I diritti vengono specificati con valori definiti dal tipo **di enumerazione RIGHTS WMT. \_** È possibile selezionare più valori combinandoli con l'operatore **OR** bit per bit.

## <a name="global-constant"></a>Costante globale

g \_ wszWMDRM \_ Flags

## <a name="data-type"></a>Tipo di dati

**DWORD \_ DI \_ TIPO WMT**

## <a name="remarks"></a>Commenti

Quando si accede **all'interfaccia IWMHeaderInfo3** dell'oggetto writer, è possibile aggiungere o modificare questo valore. In altri oggetti (editor di metadati, lettore e lettore sincrono), questo valore è di sola lettura. Usare [**IWMHeaderInfo::SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) per impostare questa proprietà durante la creazione del contenuto DRM versione 1.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà DRM**](drm-properties.md)
</dt> </dl>

 

 




