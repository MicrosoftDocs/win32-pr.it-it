---
description: Definizione di proprietà personalizzate.
ms.assetid: 6adcf414-2c5a-451c-b30a-d1c161886c9a
title: Definizione di proprietà personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b78516913c898e3b3d814e96a40d227cc3cc1cc70c13a290949f91eb9f447c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119348051"
---
# <a name="defining-custom-properties"></a>Definizione di proprietà personalizzate

**Definizione di proprietà personalizzate.**

Se è necessario che il minidriver di acquisizione di immagini di Windows (WIA) definisse proprietà personalizzate, la proprietà WIA PRIVATE DEVPROP deve essere usata per le proprietà personalizzate dell'elemento radice e la proprietà \_ \_ \_ WIA PRIVATE ITEMPROP" deve essere usata per altre proprietà \_ dell'elemento. Queste costanti sono definite in *wiadef.h.*

Nell'esempio di codice seguente vengono illustrate le definizioni per tre proprietà dell'elemento radice. L'ID proprietà per la prima proprietà personalizzata dell'elemento radice, CUSTOM ROOT PROP 1, è definito in termini di \_ \_ \_ \_ \_ WIA PRIVATE DEVPROP. Gli ID proprietà per proprietà aggiuntive dell'elemento radice sono definiti in termini di \_ WIA PRIVATE \_ DEVPROP + 1, WIA \_ PRIVATE \_ DEVPROP + 2 e così via. Il modello può essere continuato se sono necessarie proprietà aggiuntive dell'elemento radice personalizzato.


```
#define CUSTOM_ROOT_PROP_1 WIA_PRIVATE_DEVPROP
#define CUSTOM_ROOT_PROP_2 (WIA_PRIVATE_DEVPROP + 1) 
#define CUSTOM_ROOT_PROP_3 (WIA_PRIVATE_DEVPROP + 2)
```



Nell'esempio seguente vengono illustrate le definizioni per tre proprietà e ID proprietà degli elementi figlio personalizzati. L'ID proprietà per la prima proprietà personalizzata dell'elemento figlio, CUSTOM CHILD PROP 1, è definito in termini \_ \_ di \_ WIA PRIVATE \_ \_ ITEMPROP. Gli ID proprietà per le proprietà aggiuntive degli elementi figlio sono definiti in termini di \_ WIA PRIVATE \_ ITEMPROP + 1 e così via. Come in precedenza, il modello può essere continuato se sono necessarie altre proprietà personalizzate dell'elemento figlio.


```
#define CUSTOM_CHILD_PROP_1 WIA_PRIVATE_ITEMPROP
#define CUSTOM_CHILD_PROP_2 (WIA_PRIVATE_ITEMPROP + 1)
#define CUSTOM_CHILD_PROP_3 (WIA_PRIVATE_ITEMPROP + 2)
```



Le proprietà WIA personalizzate devono avere nomi di proprietà personalizzati associati agli ID delle proprietà personalizzate. Nell'esempio di codice seguente vengono illustrate le definizioni per tre nomi di proprietà dell'elemento radice personalizzato. Questi nomi di proprietà vengono usati con gli ID proprietà personalizzati creati in un esempio precedente, in cui il nome della proprietà personalizzata è contenuto in CUSTOM \_ ROOT \_ PROP \_ 1 STR è associato all'ID della proprietà \_ dell'elemento radice personalizzato CUSTOM ROOT \_ PROP \_ \_ 1.


```
#define CUSTOM_ROOT_PROP_1_STR L"My First Custom Root Item Property"
#define CUSTOM_ROOT_PROP_2_STR L"My Second Custom Root Item Property"
#define CUSTOM_ROOT_PROP_3_STR L"My Third Custom Root Item Property"
```



> [!Note]  
> I nomi delle proprietà WIA *non sono* localizzati in più lingue. Ciò è dovuto al fatto che le proprietà WIA possono essere lette dalle applicazioni usando l'ID proprietà o il nome della proprietà. Se il nome viene usato, deve essere una costante, esattamente come l'ID della proprietà.

 

 

 



