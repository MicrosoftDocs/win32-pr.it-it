---
description: L'interfaccia IProvidePropertyBuilder, se implementata, consente agli oggetti di specificare gli oggetti del generatore di proprietà per le proprietà.
ms.assetid: 26557622-4a97-4db0-85ed-3f77fcb769a0
title: Interfaccia IProvidePropertyBuilder
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder:IUnknown
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: d6d82cdafbf775c7316ed882cf3776aaf216fcb82938825d8c939f21e60cc0e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750021"
---
# <a name="iprovidepropertybuilder-interface"></a>Interfaccia IProvidePropertyBuilder

**L'interfaccia IProvidePropertyBuilder,** se implementata, consente agli oggetti di specificare gli oggetti del generatore di proprietà per le proprietà. I generatori vengono richiamati da un pulsante con i puntini di sospensione ( ... ) nel visualizzatore proprietà Microsoft Visual Studio e vengono richiamati tramite ExecuteBuilder quando viene premuto \[ \] il pulsante. [](iprovidepropertybuilder-executebuilder.md) Per fornire un generatore per una determinata proprietà, restituire un GUID per il generatore di proprietà che deve essere richiamato per la proprietà corrente da [**MapPropertyToBuilder.**](iprovidepropertybuilder-mappropertytobuilder.md) I generatori vengono in genere implementati tramite finestre di dialogo modali.

La versione per questa interfaccia è 1.0. Le chiamate al metodo vengono ricevute in un endpoint assegnato dinamicamente (come descritto nella documentazione binaria di MSMQ sul mapping degli endpoint) e usano l'UUID (universalmente unique identifier) "33C0C1D8-33CF-11d3-BFF2-00C04F990235".

## <a name="members"></a>Membri

**L'interfaccia IProvidePropertyBuilder:IUnknown** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IProvidePropertyBuilder** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IProvidePropertyBuilder:IUnknown** include questi metodi.



| Metodo                                                                       | Descrizione                                                                                  |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**ExecuteBuilder**](iprovidepropertybuilder-executebuilder.md)             | Notifica a un oggetto che deve visualizzare il generatore per la proprietà specificata.<br/> |
| [**MapPropertyToBuilder**](iprovidepropertybuilder-mappropertytobuilder.md) | Controlla se un generatore deve essere associato a una determinata proprietà.<br/>         |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Vsp.dll</dt> </dl> |



 

 
