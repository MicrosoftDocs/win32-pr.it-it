---
description: Per evitare conflitti di nomi tra proprietà create da oggetti diversi, il gestore delle proprietà condivise (SPM) usa gruppi di proprietà condivise.
ms.assetid: f73d631e-2552-4358-903a-739e2df3657d
title: Gruppi di proprietà condivise
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cda375c09b164e4ed380ba7d89477f2225b5b6004f98299ec9fd9b46f80abee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029217"
---
# <a name="shared-property-groups"></a>Gruppi di proprietà condivise

Per evitare conflitti di nomi tra proprietà create da oggetti diversi, il gestore delle proprietà condivise (SPM) usa gruppi di proprietà condivise. Un gruppo di proprietà condivise è semplicemente uno spazio dei nomi per un set di proprietà condivise. Ogni proprietà all'interno di un gruppo di proprietà condivise è costituita da un nome, un valore e una posizione all'interno del gruppo di proprietà condivise. È possibile usare il nome o la posizione per recuperare il valore della proprietà. È possibile accedere e creare gruppi di proprietà condivise tramite il gestore dei gruppi di proprietà condivise.

Il modello a oggetti SPM è illustrato nella figura seguente.

![Diagramma che mostra il modello a oggetti SPM: ISharedPropertyGroupManager, ISharedPropertyGroup, in ISharedProperty.](images/1df31cd9-2fc4-48d3-ae68-cae38afb75a6.png)

Di seguito sono riportate le interfacce della gestione proprietà condivise:

-   [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager) viene usato per creare gruppi di proprietà condivise e per ottenere l'accesso ai gruppi di proprietà condivise esistenti. È possibile accedere **all'interfaccia ISharedPropertyGroupManager** creando un'istanza dell'oggetto [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md) usando [**IObjectContext::CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance) o [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

-   [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup) viene usato per creare e accedere alle proprietà condivise in un gruppo di proprietà condivise. È possibile accedere **all'interfaccia ISharedPropertyGroup** creando un [**oggetto SharedPropertyGroup**](sharedpropertygroup.md) con il [**metodo ISharedPropertyGroupManager::CreatePropertyGroup.**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) Come per qualsiasi oggetto COM, è necessario rilasciare un **oggetto SharedPropertyGroup** al termine dell'uso.

-   [**ISharedProperty viene**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty) usato per impostare o recuperare il valore di una proprietà condivisa. Una proprietà condivisa può contenere qualsiasi tipo di dati che può essere rappresentato da un elemento Variant. È possibile accedere **all'interfaccia ISharedProperty** creando un oggetto [**SharedProperty**](sharedproperty.md) con il metodo [**ISharedPropertyGroup::CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) o il metodo [**ISharedPropertyGroup::CreatePropertyByPosition.**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) È possibile creare o accedere a un oggetto **SharedProperty** solo dall'interno [**di un oggetto SharedPropertyGroup.**](sharedpropertygroup.md) Anche in questo caso, è necessario **rilasciare un oggetto SharedProperty** al termine dell'uso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Com+ Shared Gestione proprietà](com--shared-property-manager.md)
</dt> </dl>

 

 
