---
title: Interfacce dello schema
description: Interfacce dello schema
ms.assetid: b3427202-352b-4b35-877e-d28fb3d3906a
ms.tgt_platform: multiple
keywords:
- interfacce dello schema ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f414fdea2418fb92a0a3c8c9e8bf88eb6d7f00b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955087"
---
# <a name="schema-interfaces"></a>Interfacce dello schema

Il contenitore dello schema contiene un set di definizioni dello schema associate a una parte della struttura dello spazio dei nomi del provider. In genere, ogni istanza di uno spazio dei nomi dispone di un proprio schema. Nella figura seguente, ad esempio, il provider di esempio ADSI definisce un contenitore dello schema in ognuno dei nodi radice "Seattle" e "Toronto".

![contenimento dello schema](images/schemacont.png)

Per creare un'implementazione ADSI per un provider, è necessario fornire oggetti gestione schema che riflettano lo spazio dei nomi sottostante del provider e che supportano le interfacce dello schema ADSI. Di seguito è riportato un elenco delle interfacce dello schema ADSI, contenute nel contenitore dello schema.

-   [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) rappresenta le classi del servizio directory.
-   [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) rappresenta le proprietà del servizio directory con valori singoli o multipli.
-   [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) rappresenta il tipo Variant singolo.

Le interfacce definite da ADSI possono supportare proprietà e sintassi specifiche per il provider. I provider possono scegliere di estendere una definizione ADSI usando i metodi che creano e accedono alle proprietà, ad esempio, è possibile usare i metodi dell'interfaccia [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) come [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex), [**put**](/windows/desktop/api/Iads/nf-iads-iads-put) e [**PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex). I provider possono inoltre supportare proprietà aggiuntive tramite interfacce aggiuntive. Per un elenco completo delle interfacce ADSI, vedere [interfacce ADSI](adsi-interfaces.md).

Un componente del provider ADSI con uno spazio dei nomi complesso può consentire l'esistenza di più schemi in un'istanza dello spazio dei nomi, ciascuno in una parte diversa dell'albero. Tuttavia, la proprietà [**IADs:: schema**](iads-property-methods.md) di un oggetto denomina sempre la propria definizione dello schema.

 

 




