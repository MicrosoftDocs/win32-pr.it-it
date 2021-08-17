---
description: Imposta o recupera il valore di una proprietà condivisa.
ms.assetid: 19ed8d50-3ac1-408e-9f25-09f284d025f1
title: Classe SharedProperty (ComSvcs.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedProperty
api_type:
- COM
ms.openlocfilehash: 9b0daa74c7329f8dc9f2566852d863715d22fd556ce3d4674dfaf246c17504b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117915772"
---
# <a name="sharedproperty-class"></a>Classe SharedProperty

Imposta o recupera il valore di una proprietà condivisa.

Per informazioni generali sull'uso del Gestione proprietà condiviso in COM+, vedere [Com+ Shared Gestione proprietà](com--shared-property-manager.md).

## <a name="when-to-implement"></a>Quando implementare

Questa classe viene implementata da COM+.



| Requisito | Valore |
|------------|--------------------------------------------|
| Interfacce | [**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty) |



 

## <a name="when-to-use"></a>Utilizzo

Usare questa classe per accedere ai metodi di [**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty).

## <a name="remarks"></a>Commenti

È possibile creare un **oggetto SharedProperty** usando i [**metodi CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) o [**CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) di [**ISharedPropertyGroup.**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup)

Per usare questa classe da Microsoft Visual Basic, aggiungere un riferimento alla libreria dei tipi dei servizi COM+. Un oggetto SharedProperty viene creato chiamando i [**metodi CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) o [**CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) dell'oggetto [**SharedPropertyGroup.**](sharedpropertygroup.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>ComSvcs.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty)
</dt> <dt>

[**SharedPropertyGroup**](sharedpropertygroup.md)
</dt> <dt>

[**Sharedpropertygroupmanager**](sharedpropertygroupmanager.md)
</dt> </dl>

 

 




