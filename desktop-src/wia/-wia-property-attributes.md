---
description: Tutti gli oggetti elemento hanno proprietà.
ms.assetid: 00e04790-e319-41b3-b88f-8064912b91b1
title: Attributi delle proprietà (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdee1cdee48bba6183f9bcae2abc521ac9f53dfb33eec544ab3ed6bead4947b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007531"
---
# <a name="property-attributes-wia"></a>Attributi delle proprietà (WIA)

Tutti gli oggetti elemento hanno proprietà. Le proprietà hanno attributi. Ad esempio, gli attributi della proprietà indicano se una proprietà viene letta, scritta o eliminata. Indicano anche i valori di proprietà validi. Le costanti seguenti sono attributi di proprietà validi: 

| Attributo property        | Significato                                                                                                  |
|---------------------------|----------------------------------------------------------------------------------------------------------|
| WIA \_ PROP \_ MEMORIZZABILE NELLA CACHE      | Il dispositivo può memorizzare nella cache il valore della proprietà.                                                               |
| WIA \_ PROP \_ FLAG           | La proprietà include un elenco di valori di flag validi. I valori dei flag vengono combinati usando un'operazione **OR** bit per bit. |
| ELENCO DI PROPRIETÀ WIA \_ \_           | La proprietà include un elenco di valori validi.                                                                 |
| WIA \_ PROP \_ NONE           | Alla proprietà non sono associati valori validi.                                          |
| INTERVALLO DI PROPRIETÀ WIA \_ \_          | La proprietà ha un intervallo di valori validi.                                                                |
| WIA \_ PROP \_ READ           | L'applicazione può leggere il valore della proprietà.                                                           |
| WIA \_ PROP \_ RW             | L'applicazione può leggere e scrivere il valore della proprietà.                                                 |
| È NECESSARIA LA SINCRONIZZAZIONE DI WIA \_ \_ \_ PROP | Non usare.                                                                                              |
| SCRITTURA DI PROPRIETÀ WIA \_ \_          | L'applicazione può scrivere il valore della proprietà.                                                          |



 

 

 



