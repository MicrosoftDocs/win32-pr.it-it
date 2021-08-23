---
description: In questa sezione vengono descritte le Windows del sistema di proprietà.
ms.assetid: d81fe8df-9fd6-4ace-a47f-214cbba6f30c
title: Interfacce (Windows proprietà)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d608e1b994541667847d755e95966b6ea2770c2d0c73ce86ef8fbd79b8c9dc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600121"
---
# <a name="interfaces-windows-property-system"></a>Interfacce (Windows proprietà)

In questa sezione vengono descritte le Windows del sistema di proprietà.



| Argomento                                                                                        | Contenuto                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPropertyChange**](/windows/win32/api/propsys/nn-propsys-ipropertychange)                                                 | Espone un metodo che incapsula una modifica a una singola proprietà.                                                                                                                                                                                                                                                                                                                          |
| [**IPropertyChangeArray**](/windows/win32/api/propsys/nn-propsys-ipropertychangearray)                                       | Espone metodi per diverse operazioni di modifica multiple che possono essere passate a [**IFileOperation.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileoperation)                                                                                                                                                                                                                                                                   |
| [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription)                                       | Espone i metodi che enumerano e recuperano i dettagli della descrizione delle singole proprietà.                                                                                                                                                                                                                                                                                                       |
| [**IPropertyDescription2**](/windows/win32/api/propsys/nn-propsys-ipropertydescription2)                                     | Espone i metodi che enumerano e recuperano i dettagli della descrizione delle singole proprietà.                                                                                                                                                                                                                                                                                                       |
| [**IPropertyDescriptionAliasInfo**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionaliasinfo)                     | Espone metodi per ottenere le proprietà delle colonne "ordina per" per un elemento. Questa interfaccia viene usata dagli oggetti dell'interfaccia utente che vogliono recuperare le colonne di ordinamento primarie o secondarie per una determinata proprietà.                                                                                                                                                                                                |
| [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist)                               | Espone metodi che estraggono informazioni da una raccolta di descrizioni di proprietà presentate come elenco.                                                                                                                                                                                                                                                                                   |
| [**IPropertyDescriptionRelatedPropertyInfo**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionrelatedpropertyinfo) | Fornisce un metodo che ritenta [**un'interfaccia IPropertyDescription.**](/windows/win32/api/propsys/nn-propsys-ipropertydescription)                                                                                                                                                                                                                                                                                       |
| [**IPropertyDescriptionSearchInfo**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionsearchinfo)                   | Espone informazioni correlate alla ricerca per una proprietà. Le informazioni fornite da questa interfaccia provengono dallo schema [propertyDescription,](./propdesc-schema-propertydescription.md) elemento [searchInfo](./propdesc-schema-searchinfo.md) per una determinata proprietà. Queste informazioni vengono usate dall'Windows Search Indexer. La maggior parte delle applicazioni chiamanti non dovrà chiamare questa interfaccia. |
| [**IPropertyEnumType**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype)                                             | Espone metodi che estraggono dati dalle informazioni di enumerazione. [**IPropertyEnumType consente**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype) di accedere agli elementi [enum](./propdesc-schema-enum.md) ed [enumRange](./propdesc-schema-enumrange.md) nello [schema](./propdesc-schema-entry.md) delle proprietà in modo programmatico in fase di esecuzione.                                                                 |
| [**IPropertyEnumType2**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype2)                                           | Espone metodi che estraggono dati dalle informazioni di enumerazione. [**IPropertyEnumType2**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype2) estende [**IPropertyEnumType**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype).                                                                                                                                                                                                               |
| [**IPropertyEnumTypeList**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtypelist)                                     | Espone metodi che enumerano i valori possibili per una proprietà.                                                                                                                                                                                                                                                                                                                         |
| [**Ipropertystore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)                                                   | Espone metodi per l'enumerazione, il recupero e l'impostazione dei valori delle proprietà.                                                                                                                                                                                                                                                                                                                     |
| [**IPropertyStoreCache**](/windows/win32/api/propsys/nn-propsys-ipropertystorecache)                                         | Espone metodi che consentono a un gestore di gestire vari stati per ogni proprietà.                                                                                                                                                                                                                                                                                                           |
| [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities)                           | Espone un metodo che determina se una proprietà può essere modificata nell'interfaccia utente dall'utente.                                                                                                                                                                                                                                                                                                   |
| [**IPropertyStoreFactory**](/windows/win32/api/propsys/nn-propsys-ipropertystorefactory)                                     | Espone metodi per ottenere un [**oggetto IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)                                                                                                                                                                                                                                                                                                               |
| [**IPropertySystem**](/windows/win32/api/propsys/nn-propsys-ipropertysystem)                                                 | Espone metodi che ottengono descrizioni delle proprietà, registrano e annullano la registrazione degli schemi di proprietà, enumerano le descrizioni delle proprietà e formattano i valori delle proprietà in modo rigoroso per i tipi.                                                                                                                                                                                                                |
| [**IPropertyUI**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipropertyui)                                                         | Gli sviluppatori devono invece [**usare IPropertyDescription.**](/windows/win32/api/propsys/nn-propsys-ipropertydescription)                                                                                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà Windows](props.md)
</dt> <dt>

[Schema di descrizione della proprietà](property-description-schema.md)
</dt> <dt>

[Set di proprietà](property-sets.md)
</dt> <dt>

[Funzioni](functions.md)
</dt> <dt>

[Strutture](structures.md)
</dt> <dt>

[Costanti, enumerazioni e flag](constants--enumerations--and-flags.md)
</dt> </dl>

 

 
