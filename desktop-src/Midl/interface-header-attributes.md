---
title: Attributi dell'intestazione dell'interfaccia
description: Incorporare questi attributi nell'intestazione dell'interfaccia per fornire informazioni sull'intera interfaccia.
ms.assetid: 5e30c902-1a55-4afd-afba-93fcc9e75033
keywords:
- MIDL, attributi, intestazione dell'interfaccia IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3e5fc25a0e441b092749872a1b4d4735d483cae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044520"
---
# <a name="interface-header-attributes"></a>Attributi dell'intestazione dell'interfaccia

Incorporare questi attributi nell'intestazione dell'interfaccia per fornire informazioni sull'intera interfaccia.



| Attributo                                   | Utilizzo                                                                                                                                                                                                                                            |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_UUID asincrono**](async-uuid.md)           | Indica al compilatore MIDL di definire le versioni sincrone e asincrone di un'interfaccia COM.                                                                                                                                               |
| [**uuid**](uuid.md)                        | Designa un valore a 128 bit che distingue una particolare interfaccia da tutti gli altri. Il valore effettivo può rappresentare un GUID, un CLSID o un IID.                                                                                                 |
| [**locale**](local.md)                      | Indica al compilatore MIDL di generare solo file di intestazione. Un'interfaccia deve avere un attributo [**UUID**](uuid.md) o [**local**](local.md) .                                                                                             |
| [**MS \_ Union**](-ms-union.md)              | Controlla l'allineamento del rapporto di recapito delle unioni non incapsulate. Usare per la compatibilità con le versioni precedenti delle interfacce basate su MIDL 1,0 o 2,0.                                                                                                                   |
| [**oggetto**](object.md)                    | Identifica l'interfaccia come interfaccia COM e indica al compilatore MIDL di generare codice proxy/stub anziché stub client e server RPC.                                                                                                    |
| [**Versione**](version.md)                  | Identifica una particolare versione di un'interfaccia nei casi in cui esistano più versioni dell'interfaccia. Poiché le interfacce COM non sono modificabili, non è possibile usare l'attributo [**Version**](version.md) in un'interfaccia [**oggetto**](object.md) . |
| [**puntatore \_ predefinito**](pointer-default.md) | Specifica il tipo di puntatore predefinito per tutti i puntatori tranne quelli inclusi negli elenchi di parametri. Il tipo predefinito può essere [**Unique**](unique.md), [**ref**](ref.md)o [**ptr**](ptr.md).                                                   |
| [**endpoint**](endpoint.md)                | Specifica un endpoint statico (noto) in cui un'applicazione server resterà in ascolto delle chiamate a procedure remote.                                                                                                                                   |



 

Vedere [attributi della libreria dei tipi](type-library-attributes.md) per attributi di interfaccia, ad esempio [**Dual**](dual.md) e [**oleautomation**](oleautomation.md), specifici delle interfacce definite o a cui si fa riferimento all'interno di un'istruzione di libreria.

 

 




