---
description: Tutti gli oggetti Item dispongono di proprietà.
ms.assetid: 00e04790-e319-41b3-b88f-8064912b91b1
title: Attributi di proprietà (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c635cb0d4e21fe2a1d65a3f21254f8e9c04d64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485060"
---
# <a name="property-attributes-wia"></a>Attributi di proprietà (WIA)

Tutti gli oggetti Item dispongono di proprietà. Le proprietà hanno attributi. Ad esempio, gli attributi delle proprietà indicano se una proprietà viene letta, scritta o eliminata. Indica inoltre i valori validi della proprietà. Le costanti seguenti sono attributi di proprietà validi: 

| Attributo Property        | Significato                                                                                                  |
|---------------------------|----------------------------------------------------------------------------------------------------------|
| inseribile \_ \_ nella cache WIA      | Il dispositivo può memorizzare nella cache il valore della proprietà.                                                               |
| \_flag di prop WIA \_           | La proprietà dispone di un elenco di valori di flag validi. I valori dei flag vengono combinati tramite **un'operazione or** bit per bit. |
| \_elenco di oggetti WIA \_           | La proprietà dispone di un elenco di valori validi.                                                                 |
| \_None Prop \_ nessuno           | Alla proprietà non è associato alcun valore valido.                                          |
| \_intervallo di oggetti WIA \_          | La proprietà ha un intervallo di valori validi.                                                                |
| \_lettura della prop di WIA \_           | L'applicazione è in grado di leggere il valore della proprietà.                                                           |
| WIA \_ prop \_ RW             | L'applicazione è in grado di leggere e scrivere il valore della proprietà.                                                 |
| \_ \_ richiesta sincronizzazione Prop \_ WIA | Non usare.                                                                                              |
| \_scrittura della prop WIA \_          | L'applicazione può scrivere il valore della proprietà.                                                          |



 

 

 



