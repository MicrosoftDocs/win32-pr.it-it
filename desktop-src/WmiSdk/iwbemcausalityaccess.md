---
description: Tiene traccia delle richieste figlio generate da una richiesta padre.
ms.assetid: e1d98eae-6fc1-489b-aa8b-2e86bac5c65a
ms.tgt_platform: multiple
title: Interfaccia IWbemCausalityAccess (Wbemint.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: a8c71d5b5f59a3b59fe3b639104bfa1fa2dcf9cd35764e37984759827ff7e92b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131393"
---
# <a name="iwbemcausalityaccess-interface"></a>Interfaccia IWbemCausalityAccess

**L'interfaccia IWbemCausalityAccess** tiene traccia delle richieste figlio generate da una richiesta padre. È possibile ottenere un **oggetto IWbemCausalityAccess** usando un'interfaccia di query (QI) per [**IWbemContext.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) Ogni richiesta è identificata da un identificatore univoco globale (GUID) e può avere una richiesta padre o può essere una richiesta principale. Un GUID è un numero univoco a 128 bit. Ad esempio, 5b2fc63a-8af4-44cb-960c-aefdced908d6.

## <a name="members"></a>Membri

**L'interfaccia IWbemCausalityAccess** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWbemCausalityAccess** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IWbemCausalityAccess** include questi metodi.



| Metodo                                                    | Descrizione                                                                                                                                                             |
|:----------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetRequestId**](iwbemcausalityaccess-getrequestid.md) | Restituisce un identificatore GUID univoco per una richiesta.<br/>                                                                                                              |
| [**IsChildOf**](iwbemcausalityaccess-ischildof.md)       | Determina se una richiesta è figlio di una richiesta padre specificata. Una richiesta padre può avere più richieste figlio, ognuna identificata da un valore GUID univoco.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemint.h</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Fastprox.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[API COM per WMI](com-api-for-wmi.md)
</dt> </dl>

 

