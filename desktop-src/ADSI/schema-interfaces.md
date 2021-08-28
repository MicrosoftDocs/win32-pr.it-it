---
title: Interfacce dello schema
description: Interfacce dello schema
ms.assetid: b3427202-352b-4b35-877e-d28fb3d3906a
ms.tgt_platform: multiple
keywords:
- interfacce dello schema ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dfa22a32a4d93c36a7419d48ea6127c2345ffdea62686147d1ba08c41ea7992
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770556"
---
# <a name="schema-interfaces"></a>Interfacce dello schema

Il contenitore dello schema contiene un set di definizioni dello schema associate a una parte dell'albero dello spazio dei nomi del provider. In genere, ogni istanza di uno spazio dei nomi ha un proprio schema. Nella figura seguente, ad esempio, il provider di esempio ADSI definisce un contenitore dello schema in ognuno dei nodi radice "Seattle" e "Toronto".

![contenimento dello schema](images/schemacont.png)

Per creare un'implementazione ADSI per un provider, è necessario fornire oggetti di gestione dello schema che riflettano lo spazio dei nomi sottostante del provider e che supportano le interfacce dello schema ADSI. Di seguito è riportato un elenco delle interfacce dello schema ADSI, contenute nel contenitore dello schema.

-   [**IADsClass rappresenta**](/windows/desktop/api/Iads/nn-iads-iadsclass) le classi del servizio directory.
-   [**IADsProperty rappresenta**](/windows/desktop/api/Iads/nn-iads-iadsproperty) le proprietà del servizio directory con valori singoli o multipli.
-   [**IADsSyntax rappresenta**](/windows/desktop/api/Iads/nn-iads-iadssyntax) il singolo tipo VARIANT.

Le interfacce definite da ADSI possono supportare proprietà e sintassi specifiche per il provider. I provider possono scegliere di estendere una definizione ADSI usando i metodi che creano e accedono alle proprietà, ad esempio è possibile usare i metodi dell'interfaccia [**IADs,**](/windows/desktop/api/Iads/nn-iads-iads) ad esempio [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex), [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put) e [**PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex). I provider possono anche supportare proprietà aggiuntive tramite interfacce aggiuntive. Per un elenco completo delle interfacce ADSI, vedere [Interfacce ADSI](adsi-interfaces.md).

Un componente provider ADSI con uno spazio dei nomi complesso potrebbe consentire l'esistenza di più schemi in un'istanza dello spazio dei nomi, ognuno in una parte diversa dell'albero. La [**proprietà IADs::Schema**](iads-property-methods.md) di un oggetto, tuttavia, nomi sempre la propria definizione dello schema.

 

 




