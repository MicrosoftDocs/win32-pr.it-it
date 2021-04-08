---
description: Crea gruppi di proprietà condivisi e per ottenere l'accesso ai gruppi di proprietà condivisi esistenti.
ms.assetid: 4ba05806-afda-4926-8ca4-abbf15ed8278
title: Classe SharedPropertyGroupManager (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedPropertyGroupManager
api_type:
- COM
ms.openlocfilehash: 680c5caef996d329e18192193f30841f61f02f27
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877621"
---
# <a name="sharedpropertygroupmanager-class"></a>Classe SharedPropertyGroupManager

Crea gruppi di proprietà condivisi e per ottenere l'accesso ai gruppi di proprietà condivisi esistenti.

Per ulteriori informazioni sull'utilizzo del Gestione proprietà condiviso in COM+, vedere [com+ shared gestione proprietà](com--shared-property-manager.md).

## <a name="when-to-implement"></a>Quando implementare

Questa classe è implementata da COM+.



| Requisito | Valore |
|------------|--------------------------------------------------------------------|
| CLSID      | \_SHAREDPROPERTYGROUPMANAGER CLSID                                  |
| ProgID     | L "MTxSpm. SharedPropertyGroupManager"                               |
| Interfacce | [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager) |



 

## <a name="when-to-use"></a>Utilizzo

Usare questa classe per accedere ai metodi di [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager).

## <a name="remarks"></a>Commenti

Per creare questo oggetto, chiamare [**IObjectContext:: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).

Per utilizzare questa classe da Microsoft Visual Basic, aggiungere un riferimento alla libreria dei tipi di servizi COM+. Un oggetto SharedPropertyGroupManager può essere dichiarato con "COMSVCSLib. SharedPropertyGroupManager" come nome della classe.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>ComSvcs. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager)
</dt> <dt>

[**SharedProperty**](sharedproperty.md)
</dt> <dt>

[**SharedPropertyGroup**](sharedpropertygroup.md)
</dt> </dl>

 

 




