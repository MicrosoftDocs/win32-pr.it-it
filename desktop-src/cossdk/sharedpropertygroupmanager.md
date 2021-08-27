---
description: Crea gruppi di proprietà condivise e per ottenere l'accesso ai gruppi di proprietà condivise esistenti.
ms.assetid: 4ba05806-afda-4926-8ca4-abbf15ed8278
title: Classe SharedPropertyGroupManager (ComSvcs.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedPropertyGroupManager
api_type:
- COM
ms.openlocfilehash: ac05dcc813192a9ea1bf1f1f4e5ad63ed72eca6874de855ac3f4582af51680f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120361"
---
# <a name="sharedpropertygroupmanager-class"></a>Classe SharedPropertyGroupManager

Crea gruppi di proprietà condivise e per ottenere l'accesso ai gruppi di proprietà condivise esistenti.

Per altre informazioni sull'uso del Gestione proprietà condiviso in COM+, vedere [Com+ Shared Gestione proprietà](com--shared-property-manager.md).

## <a name="when-to-implement"></a>Quando implementare

Questa classe viene implementata da COM+.



| Requisito | Valore |
|------------|--------------------------------------------------------------------|
| CLSID      | CLSID \_ SharedPropertyGroupManager                                  |
| ProgID     | L"MTxSpm.SharedPropertyGroupManager"                               |
| Interfacce | [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager) |



 

## <a name="when-to-use"></a>Utilizzo

Usare questa classe per accedere ai metodi di [**ISharedPropertyGroupManager.**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager)

## <a name="remarks"></a>Commenti

Per creare questo oggetto, chiamare [**IObjectContext::CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).

Per usare questa classe da Microsoft Visual Basic, aggiungere un riferimento alla libreria dei tipi dei servizi COM+. Un oggetto SharedPropertyGroupManager può essere dichiarato usando "COMSVCSLib.SharedPropertyGroupManager" come nome della classe.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>ComSvcs.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager)
</dt> <dt>

[**Proprietà condivisa**](sharedproperty.md)
</dt> <dt>

[**SharedPropertyGroup**](sharedpropertygroup.md)
</dt> </dl>

 

 




