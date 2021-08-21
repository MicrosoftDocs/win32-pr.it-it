---
title: Proprietà pluginName di ItsPubPlugin
description: Recupera il nome del plug-in.
ms.assetid: c1ea46b6-fac6-4140-a278-cb04ee9af739
ms.tgt_platform: multiple
keywords:
- Proprietà pluginName Servizi Desktop remoto
- proprietà pluginName Servizi Desktop remoto, interfaccia ItsPubPlugin
- ItsPubPlugin interface Servizi Desktop remoto proprietà pluginName
topic_type:
- apiref
api_name:
- ItsPubPlugin.pluginName
- ItsPubPlugin.get_pluginName
api_location:
- Cpubplugin.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa1cd3103e901255a6226db3e128e81bb17c02e6b586a48ca434ed44932861c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118128640"
---
# <a name="itspubpluginpluginname-property"></a>Proprietà ItsPubPlugin::p luginName

Recupera il nome del plug-in.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_pluginName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valore proprietà

Puntatore a una **variabile BSTR** per ricevere il nome del plug-in.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                         |
| Idl<br/>                      | <dl> <dt>Cpubplugin.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ItsPubPlugin**](/windows/desktop/api/tspubplugincom/nn-tspubplugincom-itspubplugin)
</dt> </dl>

 

 





