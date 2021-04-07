---
title: CFSTR_DSQUERYPARAMS (DSQuery. h)
description: Il \_ formato degli Appunti DSQUERYPARAMS di CFSTR fornisce un handle di memoria globale (HGLOBAL) che contiene una struttura DSQUERYPARAMS.
ms.assetid: bb8aea98-8309-42bf-993d-fa408bb4deb2
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- CFSTR_DSQUERYPARAMS
api_location:
- DSQuery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a330d228778f34118d232b2004e7294ab493ed77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964058"
---
# <a name="cfstr_dsqueryparams"></a>\_DSQUERYPARAMS CFSTR

<dl> <dt>

<span id="CFSTR_DSQUERYPARAMS"></span><span id="cfstr_dsqueryparams"></span>**\_DSQUERYPARAMS CFSTR**
</dt> <dd> <dl> <dt>

"DsQueryParameters"
</dt> <dt>



Il formato degli Appunti **\_ DSQUERYPARAMS di CFSTR** è supportato dal [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) fornito dal metodo [**ICommonQuery:: openQueryWindow**](/windows/win32/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow) . Il formato degli Appunti **\_ DSQUERYPARAMS di CFSTR** fornisce un handle di memoria globale (**HGLOBAL**) che contiene una struttura [**DSQUERYPARAMS**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams) .


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>DSQuery. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)
</dt> <dt>

[**ICommonQuery::OpenQueryWindow**](/windows/win32/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow)
</dt> <dt>

[**DSQUERYPARAMS**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams)
</dt> </dl>

 

