---
description: Recupera le informazioni per le applicazioni importate.
ms.assetid: 9ed4bc3f-3490-4c36-ba94-bc803886a4d2
title: Raccolta FilesForImport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FilesForImport
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8e7ba3b0bd44cf2f6bb40ecf89f86dd68c21cf3c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127143"
---
# <a name="filesforimport-collection"></a>Raccolta FilesForImport

Recupera le informazioni per le applicazioni importate.

Questa raccolta supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membri

La raccolta **FilesForImport** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="related-collections"></a>Raccolte correlate

È possibile passare da questa raccolta a una delle raccolte seguenti:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

È possibile passare a questa raccolta dalle raccolte seguenti:

-   [**Radice**](root.md)

## <a name="properties"></a>Proprietà

Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:

-   [ApplicationFileName](#applicationfilename)
-   [ApplicationName](#applicationname)
-   [Descrizione](#partitiondescription)
-   [FileName](#applicationfilename)
-   [HasUsers](#hasusers)
-   [IsProxy](#isproxy)
-   [IsService](#isservice)
-   [PartitionDescription](#partitiondescription)
-   [PartitionID](#partitionid)
-   [PartitionName](#partitionname)

### <a name="applicationfilename"></a>ApplicationFileName



| Voce | Valore |
|----------------|------------------------------------------------------------------------------|
| Descrizione    | Nome del file MSI che contiene l'applicazione che può essere importata. |
| Access         | ReadOnly                                                                     |
| Type           | string                                                                       |
| Predefinito        | N/D                                                                          |
| Sistema minimo | Windows XP                                                                   |



 

### <a name="applicationname"></a>ApplicationName



| Voce | Valore |
|----------------|------------------------------|
| Descrizione    | Nome dell'applicazione. |
| Access         | ReadOnly                     |
| Type           | string                       |
| Predefinito        | ""                           |
| Sistema minimo | Windows XP                   |



 

### <a name="description"></a>Descrizione



| Voce | Valore |
|----------------|-----------------------------------|
| Descrizione    | Descrizione dell'applicazione. |
| Access         | ReadOnly                          |
| Type           | string                            |
| Predefinito        | ""                                |
| Sistema minimo | Windows XP                        |



 

### <a name="filename"></a>FileName



| Voce | Valore |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Nome della DLL o del file EXE che contiene l'applicazione. Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta. |
| Access         | ReadOnly                                                                                                                                                                                                                              |
| Type           | string                                                                                                                                                                                                                                |
| Predefinito        | ""                                                                                                                                                                                                                                    |
| Sistema minimo | Windows XP                                                                                                                                                                                                                            |



 

### <a name="hasusers"></a>HasUsers



| Voce | Valore |
|----------------|--------------------------------------------------|
| Descrizione    | Indica se l'applicazione dispone di utenti. |
| Access         | ReadOnly                                         |
| Tipo           | Bool                                             |
| Predefinito        | Falso                                            |
| Sistema minimo | Windows XP                                       |



 

### <a name="isproxy"></a>IsProxy



| Voce | Valore |
|----------------|-----------------------------------------------|
| Descrizione    | Indica se l'applicazione è un proxy. |
| Access         | ReadOnly                                      |
| Tipo           | Bool                                          |
| Predefinito        | Falso                                         |
| Sistema minimo | Windows XP                                    |



 

### <a name="isservice"></a>IsService



| Voce | Valore |
|----------------|-------------------------------------------------|
| Descrizione    | Indica se l'applicazione è un servizio. |
| Access         | ReadOnly                                        |
| Tipo           | Bool                                            |
| Predefinito        | Falso                                           |
| Sistema minimo | Windows XP                                      |



 

### <a name="partitiondescription"></a>PartitionDescription



| Voce | Valore |
|----------------|-----------------------------------------------|
| Descrizione    | Descrizione della partizione dell'applicazione. |
| Access         | ReadOnly                                      |
| Type           | string                                        |
| Predefinito        | ""                                            |
| Sistema minimo | Windows Server 2003                           |



 

### <a name="partitionid"></a>PartitionID



| Voce | Valore |
|----------------|------------------------------------------|
| Descrizione    | GUID della partizione dell'applicazione. |
| Access         | ReadOnly                                 |
| Type           | string                                   |
| Predefinito        | ""                                       |
| Sistema minimo | Windows Server 2003                      |



 

### <a name="partitionname"></a>PartitionName



| Voce | Valore |
|----------------|------------------------------------------|
| Descrizione    | Nome della partizione dell'applicazione. |
| Access         | ReadOnly                                 |
| Type           | string                                   |
| Predefinito        | ""                                       |
| Sistema minimo | Windows Server 2003                      |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolte di amministrazione COM+](com--administration-collections.md)
</dt> </dl>

 

 
