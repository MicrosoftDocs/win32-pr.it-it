---
description: Per evitare conflitti di nomi tra proprietà create da oggetti diversi, il gestore di proprietà condivise (SPM) utilizza i gruppi di proprietà condivisi.
ms.assetid: f73d631e-2552-4358-903a-739e2df3657d
title: Gruppi di proprietà condivise
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776dafe5c7e9752ce3ed1c88b01fd909b4b145de
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "103761111"
---
# <a name="shared-property-groups"></a>Gruppi di proprietà condivise

Per evitare conflitti di nomi tra proprietà create da oggetti diversi, il gestore di proprietà condivise (SPM) utilizza i gruppi di proprietà condivisi. Un gruppo di proprietà condiviso è semplicemente uno spazio dei nomi per un set di proprietà condivise. Ogni proprietà all'interno di un gruppo di proprietà condiviso è costituita da un nome, da un valore e da una posizione all'interno del gruppo di proprietà condiviso. È possibile utilizzare il nome o la posizione per recuperare il valore della proprietà. È possibile accedere e creare gruppi di proprietà condivisi tramite il gestore del gruppo di proprietà condiviso.

Il modello a oggetti SPM è illustrato nella figura seguente.

![Diagramma che mostra il modello a oggetti SPM: ISharedPropertyGroupManager, ISharedPropertyGroup, ISharedProperty.](images/1df31cd9-2fc4-48d3-ae68-cae38afb75a6.png)

Di seguito sono riportate le interfacce di gestione proprietà condivise:

-   [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager) viene utilizzato per creare gruppi di proprietà condivisi e per ottenere l'accesso ai gruppi di proprietà condivisi esistenti. Per accedere all'interfaccia **ISharedPropertyGroupManager** , è possibile creare un'istanza dell'oggetto [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md) utilizzando [**IObjectContext:: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance) o [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

-   [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup) viene utilizzato per creare e accedere alle proprietà condivise in un gruppo di proprietà condivise. Per accedere all'interfaccia **ISharedPropertyGroup** , è possibile creare un oggetto [**SharedPropertyGroup**](sharedpropertygroup.md) con il metodo [**ISharedPropertyGroupManager:: CreatePropertyGroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) . Come per qualsiasi oggetto COM, è necessario rilasciare un oggetto **SharedPropertyGroup** al termine dell'utilizzo.

-   [**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty) viene usato per impostare o recuperare il valore di una proprietà condivisa. Una proprietà condivisa può contenere qualsiasi tipo di dati che può essere rappresentato da una variante. Per accedere all'interfaccia **ISharedProperty** , è possibile creare un oggetto [**SharedProperty**](sharedproperty.md) con il metodo [**ISharedPropertyGroup:: CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) o il metodo [**ISharedPropertyGroup:: CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) . È possibile creare un oggetto **SharedProperty** o accedervi solo dall'interno di un oggetto [**SharedPropertyGroup**](sharedpropertygroup.md) . Anche in questo caso, è necessario rilasciare un oggetto **SharedProperty** al termine dell'utilizzo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione proprietà condivise COM+](com--shared-property-manager.md)
</dt> </dl>

 

 
