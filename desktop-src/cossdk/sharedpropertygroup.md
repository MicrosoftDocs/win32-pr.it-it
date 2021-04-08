---
description: Consente di creare e accedere alle proprietà condivise in un gruppo di proprietà condivise.
ms.assetid: 20fd32f0-b2b2-4bed-8c59-1d1fdc8a399e
title: Classe SharedPropertyGroup (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedPropertyGroup
api_type:
- COM
ms.openlocfilehash: a3fff14043d67b96db99334c7bec1afee2577f7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748170"
---
# <a name="sharedpropertygroup-class"></a>Classe SharedPropertyGroup

Consente di creare e accedere alle proprietà condivise in un gruppo di proprietà condivise.

Per ulteriori informazioni sull'utilizzo del Gestione proprietà condiviso in COM+, vedere [com+ shared gestione proprietà](com--shared-property-manager.md).

## <a name="when-to-implement"></a>Quando implementare

Questa classe è implementata da COM+.



| Requisito | Valore |
|------------|------------------------------------------------------|
| Interfacce | [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup) |



 

## <a name="when-to-use"></a>Utilizzo

Usare questa classe per accedere ai metodi di [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup).

## <a name="remarks"></a>Commenti

È possibile creare un oggetto **SharedPropertyGroup** usando il metodo [**CreatePropertyGroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) di [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager).

Per utilizzare questa classe da Microsoft Visual Basic, aggiungere un riferimento alla libreria dei tipi di servizi COM+. Un oggetto SharedPropertyGroup viene creato chiamando il metodo [**CreatePropertyGroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) dell'oggetto [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>ComSvcs. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup)
</dt> <dt>

[**SharedProperty**](sharedproperty.md)
</dt> <dt>

[**SharedPropertyGroupManager**](sharedpropertygroupmanager.md)
</dt> </dl>

 

 




