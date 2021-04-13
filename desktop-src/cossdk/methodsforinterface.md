---
description: Contiene un oggetto per ogni metodo sull'interfaccia a cui è correlata la raccolta.
ms.assetid: e64b007f-e44d-4b6b-97b2-1e017c5a7dbe
title: Raccolta MethodsForInterface
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MethodsForInterface
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6057d06d4a67222095d5bb0b5ae6da0d603fb4ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401512"
---
# <a name="methodsforinterface-collection"></a>Raccolta MethodsForInterface

Contiene un oggetto per ogni metodo sull'interfaccia a cui è correlata la raccolta.

Questa raccolta non supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membri

La raccolta **MethodsForInterface** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="related-collections"></a>Raccolte correlate

È possibile passare da questa raccolta a una delle raccolte seguenti:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**RolesForMethod**](rolesformethod.md)

È possibile passare a questa raccolta dalle raccolte seguenti:

-   [**InterfacesForComponent**](interfacesforcomponent.md)

## <a name="properties"></a>Proprietà

Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:

-   [Completamento automatico](#autocomplete)
-   [CLSID](#clsid)
-   [Descrizione](#description)
-   [IID](#iid)
-   [Index](#index)
-   [Nome](#name)

### <a name="autocomplete"></a>AutoComplete



| Voce | Valore |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Determina se l'oggetto viene disattivato automaticamente quando il metodo viene completato, senza il metodo Tocomplete o SetAbort che viene necessariamente chiamato. Questa operazione ha effetto solo sull'impostazione predefinita del bit "Done" di attivazione JIT all'avvio del metodo. Questo bit può essere reimpostato (come con il metodo Tocomplete o SetAbort) nel metodo per eseguire l'override del valore predefinito. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                  |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                       |
| Predefinito        | Falso                                                                                                                                                                                                                                                                                                                                      |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                                                                                                                               |



 

### <a name="clsid"></a>CLSID



| Voce | Valore |
|----------------|---------------------------|
| Descrizione    | GUID per il componente. |
| Access         | ReadOnly                  |
| Type           | string                    |
| Predefinito        | N/D                       |
| Sistema minimo | Windows 2000              |



 

### <a name="description"></a>Descrizione



| Voce | Valore |
|----------------|------------------------------|
| Descrizione    | Descrizione del metodo. |
| Access         | ReadWrite                    |
| Type           | string                       |
| Predefinito        | ""                           |
| Sistema minimo | Windows 2000                 |



 

### <a name="iid"></a>IID



| Voce | Valore |
|----------------|---------------------------|
| Descrizione    | GUID per l'interfaccia. |
| Access         | ReadOnly                  |
| Type           | string                    |
| Predefinito        | N/D                       |
| Sistema minimo | Windows 2000              |



 

### <a name="index"></a>Indice



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Identificatore di invio del metodo. Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) viene chiamato su un oggetto di questa raccolta. |
| Access         | ReadOnly                                                                                                                                                        |
| Tipo           | **DWORD**                                                                                                                                                       |
| Predefinito        | N/D                                                                                                                                                             |
| Sistema minimo | Windows 2000                                                                                                                                                    |



 

### <a name="name"></a>Nome



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Nome del metodo. Questa proprietà viene restituita quando il metodo della proprietà [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta. |
| Access         | ReadOnly                                                                                                                                           |
| Type           | string                                                                                                                                             |
| Predefinito        | N/D                                                                                                                                                |
| Sistema minimo | Windows 2000                                                                                                                                       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolte di amministrazione COM+](com--administration-collections.md)
</dt> </dl>

 

 
