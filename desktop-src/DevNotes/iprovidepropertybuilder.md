---
description: L'interfaccia IProvidePropertyBuilder, quando implementata, consente agli oggetti di specificare oggetti generatore di proprietà per le proprietà.
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
ms.openlocfilehash: b93d05c3c64686b21f19ffe6262ddfd68812dd80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325213"
---
# <a name="iprovidepropertybuilder-interface"></a>Interfaccia IProvidePropertyBuilder

L'interfaccia **IProvidePropertyBuilder** , quando implementata, consente agli oggetti di specificare oggetti generatore di proprietà per le proprietà. I generatori vengono richiamati da un pulsante con i puntini di sospensione ( \[ ... \] ) nel Visualizzatore proprietà Microsoft Visual Studio e vengono richiamati tramite [**ExecuteBuilder**](iprovidepropertybuilder-executebuilder.md) quando viene premuto il pulsante. Per fornire un generatore per una determinata proprietà, restituire un GUID per il generatore di proprietà che deve essere richiamato per la proprietà corrente da [**MapPropertyToBuilder**](iprovidepropertybuilder-mappropertytobuilder.md). I generatori vengono in genere implementati tramite le finestre di dialogo modali.

La versione per questa interfaccia è 1,0. Le chiamate al metodo vengono ricevute in un endpoint assegnato dinamicamente (come descritto nella documentazione binaria MSMQ sul mapping degli endpoint) e usano l'UUID (Universally Unique Identifier) "33C0C1D8-33CF-11d3-BFF2-00C04F990235".

## <a name="members"></a>Membri

L'interfaccia **IProvidePropertyBuilder: IUnknown** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IProvidePropertyBuilder** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IProvidePropertyBuilder: IUnknown** presenta questi metodi.



| Metodo                                                                       | Descrizione                                                                                  |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**ExecuteBuilder**](iprovidepropertybuilder-executebuilder.md)             | Notifica a un oggetto che deve visualizzare il relativo generatore per la proprietà specificata.<br/> |
| [**MapPropertyToBuilder**](iprovidepropertybuilder-mappropertytobuilder.md) | Verifica se un generatore deve essere associato a una particolare proprietà.<br/>         |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Vsp.dll</dt> </dl> |



 

 
