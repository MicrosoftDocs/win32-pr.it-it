---
description: Imposta il mapping dei sottocampionamenti per l'esempio che indica i byte cancellati e crittografati nei dati di esempio.
ms.assetid: E672F53D-2083-430B-90D2-A1DA482EF9E1
title: Attributo MFSampleExtension_Encryption_SubSampleMappingSplit (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c90fb6ae22417f059bfa3268382877363178940
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309095"
---
# <a name="mfsampleextension_encryption_subsamplemappingsplit-attribute"></a>\_Attributo SubSampleMappingSplit di crittografia MFSampleExtension \_

Imposta il mapping dei sottocampionamenti per l'esempio che indica i byte cancellati e crittografati nei dati di esempio.

## <a name="data-type"></a>Tipo di dati

**BLOB**

## <a name="remarks"></a>Commenti

Il **BLOB** deve contenere una matrice di intervalli di byte come DWORD, dove ogni due DWORD crea un set. Il primo valore DWORD in ogni set è il numero di byte cancellati e il secondo valore DWORD del set è il numero di byte crittografati. Si noti che una coppia di zeri non è un set valido (il valore può essere 0, ma non entrambi). La matrice di intervalli di byte indica gli intervalli da decrittografare, inclusa la possibilità che l'intero campione non venga decrittografato. Si consiglia di non impostare questa opzione su Clear Samples, anche se è possibile ottenere lo stesso risultato impostando i valori appropriati.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come impostare \_ SubSampleMappingSplit Encryption MFSampleExtension \_ .


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
| Client minimo supportato<br/> | App \[ desktop di Windows 8.1 app \| UWP\]<br/>                                |
| Server minimo supportato<br/> | App desktop di Windows Server 2012 R2 \[ \| UWP\]<br/>                     |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[\_KeyId contenuto \_ MFSampleExtension](mfsampleextension-content-keyid.md)
</dt> </dl>

 

 




