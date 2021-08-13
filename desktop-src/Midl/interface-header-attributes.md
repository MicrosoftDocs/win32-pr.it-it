---
title: Attributi dell'intestazione dell'interfaccia
description: Incorporare questi attributi nell'intestazione dell'interfaccia per trasmettere informazioni sull'intera interfaccia.
ms.assetid: 5e30c902-1a55-4afd-afba-93fcc9e75033
keywords:
- IDL MIDL, attributi, intestazione di interfaccia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a26dac473c95625162e6dbb689f54833a166b1c58ae478654c52fededf3dd529
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642987"
---
# <a name="interface-header-attributes"></a>Attributi dell'intestazione dell'interfaccia

Incorporare questi attributi nell'intestazione dell'interfaccia per trasmettere informazioni sull'intera interfaccia.



| Attributo                                   | Uso                                                                                                                                                                                                                                            |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**async \_ uuid**](async-uuid.md)           | Indica al compilatore MIDL di definire versioni sincrone e asincrone di un'interfaccia COM.                                                                                                                                               |
| [**Uuid**](uuid.md)                        | Designa un valore a 128 bit che distingue una particolare interfaccia da tutte le altre. Il valore effettivo può rappresentare un GUID, un CLSID o un IID.                                                                                                 |
| [**Locale**](local.md)                      | Indica al compilatore MIDL di generare solo i file di intestazione. Un'interfaccia deve avere un [**attributo uuid**](uuid.md) [**o**](local.md) locale.                                                                                             |
| [**ms \_ union**](-ms-union.md)              | Controlla l'allineamento del rapporto di mancato recapito delle unioni non incapsulate. Usare per la compatibilità con le versioni precedenti con le interfacce compilate in MIDL 1.0 o 2.0.                                                                                                                   |
| [**Oggetto**](object.md)                    | Identifica l'interfaccia come interfaccia COM e indica al compilatore MIDL di generare codice proxy/stub anziché stub client e server RPC.                                                                                                    |
| [**Versione**](version.md)                  | Identifica una particolare versione di un'interfaccia nei casi in cui esistono più versioni dell'interfaccia. Poiché le interfacce COM non sono modificabili, non è possibile usare [**l'attributo version**](version.md) in un'interfaccia [**a**](object.md) oggetti. |
| [**impostazione predefinita del \_ puntatore**](pointer-default.md) | Specifica il tipo di puntatore predefinito per tutti i puntatori ad eccezione di quelli inclusi negli elenchi di parametri. Il tipo predefinito può essere [**univoco,**](unique.md) [**ref**](ref.md)o [**ptr.**](ptr.md)                                                   |
| [**Endpoint**](endpoint.md)                | Specifica un endpoint statico (noto) su cui un'applicazione server sarà in ascolto delle chiamate di procedura remota.                                                                                                                                   |



 

Vedere [Attributi della libreria dei](type-library-attributes.md) tipi per gli attributi di interfaccia, ad esempio [**dual**](dual.md) e [**oleautomation**](oleautomation.md), specifici delle interfacce definite o a cui si fa riferimento all'interno di un'istruzione della libreria.

 

 




