---
title: Creazione ed eliminazione di oggetti
description: Con ADSI, gli oggetti vengono creati ed eliminati usando l'interfaccia IADsContainer o IDirectoryObject.
ms.assetid: 4d1f7ac5-48d3-4ea9-91e4-0cd4bb2ec9f8
ms.tgt_platform: multiple
keywords:
- Creazione ed eliminazione di oggetti ADSI
- ADSI, creazione ed eliminazione di oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4730c4cc6a95ad37bfd3953474d3d488fcf05abb
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474235"
---
# <a name="creating-and-deleting-objects"></a>Creazione ed eliminazione di oggetti

Con ADSI, gli oggetti vengono creati ed eliminati usando l'interfaccia [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) o [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) .

## <a name="creating-an-object-with-iadscontainer"></a>Creazione di un oggetto con IADsContainer

**Per creare un oggetto con l'interfaccia IADsContainer**

1.  Eseguire l'associazione al contenitore che conterrà l'oggetto da creare e ottenere l'interfaccia [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) .
2.  Usare il metodo [**IADsContainer. Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) per creare un nuovo oggetto nel contenitore.
3.  Impostare i valori per tutti gli attributi obbligatori per l'oggetto usando il metodo [**IADs. Put**](/windows/desktop/api/Iads/nf-iads-iads-put) o [**IADs. PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) . Gli attributi necessari per creare un oggetto dipenderanno dal servizio directory e dal tipo di oggetto creato. Per ulteriori informazioni sulla creazione di oggetti Active Directory, vedere [creazione ed eliminazione di oggetti di Active Directory](/windows/desktop/AD/creating-and-deleting-objects-in-active-directory-domain-services).
4.  Impostare i valori per tutti gli attributi facoltativi desiderati per l'oggetto usando il metodo [**IADs. Put**](/windows/desktop/api/Iads/nf-iads-iads-put) o [**IADs. PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) .
5.  Chiamare il metodo [**IADs. seinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) per eseguire il commit dell'oggetto e dei relativi attributi. Il nuovo oggetto non viene effettivamente creato nel servizio directory sottostante fino a quando non viene chiamato il metodo **IADs. seinfo** per eseguire il commit degli attributi.

## <a name="creating-an-object-with-idirectoryobject"></a>Creazione di un oggetto con IDirectoryObject

**Per creare un oggetto con l'interfaccia IDirectoryObject**

1.  Eseguire l'associazione al contenitore che conterrà l'oggetto da creare e ottenere l'interfaccia [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) .
2.  Allocare una matrice di [**inserzioni \_ attr \_ info**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) Structures che contiene una struttura per ogni attributo da impostare quando viene creato l'oggetto.
3.  Compilare una struttura [**di \_ \_ informazioni attr ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) per ogni attributo obbligatorio per l'oggetto. Gli attributi necessari per creare un oggetto dipenderanno dal servizio directory e dal tipo di oggetto creato. Per ulteriori informazioni sulla creazione di oggetti Active Directory, vedere [creazione ed eliminazione di oggetti di Active Directory](/windows/desktop/AD/creating-and-deleting-objects-in-active-directory-domain-services).
4.  Compilare una struttura [**di \_ \_ informazioni attr ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) per ogni attributo facoltativo per l'oggetto.
5.  Usare il metodo [**IDirectoryObject:: CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) per creare l'oggetto nel contenitore. Questo metodo consente inoltre di eseguire il commit dell'oggetto nel servizio directory sottostante. Se la matrice di [**\_ \_ informazioni attr ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) non contiene tutti gli attributi obbligatori per l'oggetto, **IDirectoryObject:: CreateDSObject** avrà esito negativo.

## <a name="deleting-an-object"></a>Eliminazione di un oggetto

Per eliminare un oggetto, usare il metodo [**IADsContainer::D Elimina**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete) o [**IDirectoryObject::D eletedsobject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-deletedsobject) . Questi metodi avranno esito negativo se l'oggetto eliminato contiene oggetti figlio. Usare il metodo [**IADsDeleteOps::D eleteobject**](/windows/desktop/api/Iads/nf-iads-iadsdeleteops-deleteobject) per eliminare un contenitore e tutti gli oggetti figlio del contenitore.

Ciò che accade a un oggetto eliminato dipende dal servizio directory sottostante. Per ulteriori informazioni sull'eliminazione di oggetti Active Directory, vedere [creazione ed eliminazione di oggetti di Active Directory](/windows/desktop/AD/creating-and-deleting-objects-in-active-directory-domain-services).

 

 