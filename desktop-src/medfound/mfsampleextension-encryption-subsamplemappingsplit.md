---
description: Imposta il mapping del campione secondario per l'esempio che indica i byte non crittografati e non crittografati nei dati di esempio.
ms.assetid: E672F53D-2083-430B-90D2-A1DA482EF9E1
title: MFSampleExtension_Encryption_SubSampleMappingSplit attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19f10f845b337ab92774f36b46940fe9d5203ca3a672f573e33fbcea26e96e16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118240794"
---
# <a name="mfsampleextension_encryption_subsamplemappingsplit-attribute"></a>Attributo MFSampleExtension \_ Encryption \_ SubSampleMappingSplit

Imposta il mapping del campione secondario per l'esempio che indica i byte non crittografati e non crittografati nei dati di esempio.

## <a name="data-type"></a>Tipo di dati

**Blob**

## <a name="remarks"></a>Commenti

Il **BLOB** deve contenere una matrice di intervalli di byte come DWORD in cui ogni due DWORD crea un set. Il primo valore DWORD in ogni set è il numero di byte non crittografati e il secondo DWORD del set è il numero di byte crittografati. Si noti che una coppia di valori 0 non è un set valido (entrambi i valori possono essere 0, ma non entrambi). La matrice di intervalli di byte indica gli intervalli da decrittografare, inclusa la possibilità che l'intero esempio non debba essere decrittografato. È consigliabile non impostare questa opzione su campioni chiari, anche se è possibile ottenere lo stesso risultato impostandolo con i valori appropriati.

## <a name="examples"></a>Esempio

L'esempio seguente illustra come impostare MFSampleExtension \_ Encryption \_ SubSampleMappingSplit.


```C++
// m_spSample is a IMFSample
// pdwSubSampleMap is a DWORD*
// dwSubSampleMapSize is a DWORD

m_spSample->SetBlob( MFSampleExtension_Encryption_SubSampleMappingSplit,
                    (BYTE*)pdwSubSampleMap, 
                    dwSubSampleMapSize * sizeof(DWORD) );
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 app desktop \| app UWP\]<br/>                                |
| Server minimo supportato<br/> | Windows Server 2012 App desktop R2 \[ \| app UWP\]<br/>                     |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[MFSampleExtension \_ Content \_ KeyID](mfsampleextension-content-keyid.md)
</dt> </dl>

 

 




