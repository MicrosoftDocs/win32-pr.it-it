---
title: Funzioni (STG)
description: Le funzioni sono routine o subroutine che restituiscono un valore o valori specifici. Le funzioni di archiviazione strutturata sono descritte nelle sezioni seguenti.
ms.assetid: 5fbb05ae-594d-4fa5-97d2-a2371e94c054
keywords:
- Archiviazione strutturata Strctd STG, informazioni di riferimento, funzioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f49c091b5ba9619b649e620da7b436ebac4ccb
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/26/2021
ms.locfileid: "106334001"
---
# <a name="structured-storage-functions"></a>Funzioni di archiviazione strutturate

Le funzioni sono routine o subroutine che restituiscono un valore o valori specifici. Le funzioni di archiviazione strutturata sono descritte nelle sezioni seguenti:

-   [**CreateILockBytesOnHGlobal**](/windows/desktop/api/coml2api/nf-coml2api-createilockbytesonhglobal)
-   [**CreateStreamOnHGlobal**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal)
-   [**FmtIdToPropStgName**](/windows/desktop/api/coml2api/nf-coml2api-fmtidtopropstgname)
-   [**FreePropVariantArray**](/windows/win32/api/combaseapi/nf-combaseapi-freepropvariantarray)
-   [**GetConvertStg**](/windows/desktop/api/coml2api/nf-coml2api-getconvertstg)
-   [**GetHGlobalFromILockBytes**](/windows/desktop/api/coml2api/nf-coml2api-gethglobalfromilockbytes)
-   [**GetHGlobalFromStream**](/windows/desktop/api/combaseapi/nf-combaseapi-gethglobalfromstream)
-   [**OleConvertIStorageToOLESTREAM**](/windows/desktop/api/Ole2/nf-ole2-oleconvertistoragetoolestream)
-   [**OleConvertIStorageToOLESTREAMEx**](/windows/desktop/api/Ole2/nf-ole2-oleconvertistoragetoolestreamex)
-   [**OleConvertOLESTREAMToIStorage**](/windows/desktop/api/Ole2/nf-ole2-oleconvertolestreamtoistorage)
-   [**OleConvertOLESTREAMToIStorageEx**](/windows/desktop/api/Ole2/nf-ole2-oleconvertolestreamtoistorageex)
-   [**PropStgNameToFmtId**](/windows/desktop/api/coml2api/nf-coml2api-propstgnametofmtid)
-   [**PropVariantClear**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear)
-   [**PropVariantCopy**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantcopy)
-   [**PropVariantInit**](/windows/desktop/api/PropIdl/nf-propidl-propvariantinit)
-   [**ReadClassStg**](/windows/desktop/api/coml2api/nf-coml2api-readclassstg)
-   [**ReadClassStm**](/windows/desktop/api/coml2api/nf-coml2api-readclassstm)
-   [**ReadFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-readfmtusertypestg)
-   [**StgConvertPropertyToVariant**](/windows/desktop/api/Propidl/nf-propidl-stgconvertpropertytovariant)
-   [**SetConvertStg**](/windows/desktop/api/Ole2/nf-ole2-setconvertstg)
-   [**StgConvertVariantToProperty**](/windows/desktop/api/Propidl/nf-propidl-stgconvertvarianttoproperty)
-   [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
-   [**StgCreateDocfileOnILockBytes**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes)
-   [**StgCreatePropSetStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
-   [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
-   [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)
-   [**StgDeserializePropVariant**](/windows/desktop/api/Propvarutil/nf-propvarutil-stgdeserializepropvariant)
-   [**StgGetIFillLockBytesOnFile**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonfile)
-   [**StgGetIFillLockBytesOnILockBytes**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonilockbytes)
-   [**StgIsStorageFile**](/windows/desktop/api/coml2api/nf-coml2api-stgisstoragefile)
-   [**StgIsStorageILockBytes**](/windows/desktop/api/coml2api/nf-coml2api-stgisstorageilockbytes)
-   [**StgOpenAsyncDocfileOnIFillLockBytes**](/windows/desktop/api/Objbase/nf-objbase-stgopenasyncdocfileonifilllockbytes)
-   [**StgOpenLayoutDocfile**](/windows/desktop/api/Objbase/nf-objbase-stgopenlayoutdocfile)
-   [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
-   [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
-   [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)
-   [**StgOpenStorageOnILockBytes**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageonilockbytes)
-   [**StgPropertyLengthAsVariant**](/windows/desktop/api/Propapi/nf-propapi-stgpropertylengthasvariant)
-   [**StgSerializePropVariant**](/windows/desktop/api/propvarutil/nf-propvarutil-stgserializepropvariant)
-   [**StgSetTimes**](/windows/desktop/api/coml2api/nf-coml2api-stgsettimes)
-   [**WriteClassStg**](/windows/desktop/api/coml2api/nf-coml2api-writeclassstg)
-   [**WriteClassStm**](/windows/desktop/api/coml2api/nf-coml2api-writeclassstm)
-   [**WriteFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-writefmtusertypestg)

 

 
