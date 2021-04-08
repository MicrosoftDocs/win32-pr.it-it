---
title: Interfaccia IWMDRMLicenseQuery
description: L'interfaccia IWMDRMLicenseQuery consente alle applicazioni di eseguire query sui diritti e sullo stato delle licenze per un file protetto.
ms.assetid: 4ec8ff9f-0acb-4389-8995-65f24736491b
keywords:
- Formato Windows Media Interface IWMDRMLicenseQuery
- Interfaccia IWMDRMLicenseQuery-formato Windows Media, descritto
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6463f405bf50d4d4ecb037dc542e3af0e5b7df46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728714"
---
# <a name="iwmdrmlicensequery-interface"></a>Interfaccia IWMDRMLicenseQuery

L'interfaccia **IWMDRMLicenseQuery** consente alle applicazioni di eseguire query sui diritti e sullo stato delle licenze per un file protetto. Questa interfaccia usa l'ID chiave per eseguire query sull'archivio licenze locale.

Per ottenere un'istanza di questa interfaccia, chiamare [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md). Passare **IID \_ IWMDRMLicenseQuery** come parametro *riid* .

## <a name="members"></a>Membri

L'interfaccia **IWMDRMLicenseQuery** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMDRMLicenseQuery** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IWMDRMLicenseQuery** dispone di questi metodi.



| Metodo                                                                                | Descrizione                                                                                      |
|:--------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md)                   | Esegue una query sull'archivio licenze locale per le autorizzazioni per l'esecuzione di azioni in base all'ID chiave.<br/>         |
| [**QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md)                     | Esegue una query nell'archivio licenze locale per i dati relativi allo stato della licenza in base all'ID chiave e diritti specifici.<br/> |
| [**SetActionAllowedQueryParams**](iwmdrmlicensequery-setactionallowedqueryparams.md) | Imposta i parametri ambientali per migliorare l'accuratezza delle query sulle licenze.<br/>             |



 

## <a name="remarks"></a>Commenti

I metodi di **IWMDRMLicenseQuery** non forniscono informazioni sulle singole licenze. I dati di licenza vengono invece aggregati dal sottosistema DRM prima che vengano restituiti i risultati della query.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce**](drm-interfaces.md)
</dt> </dl>

 

