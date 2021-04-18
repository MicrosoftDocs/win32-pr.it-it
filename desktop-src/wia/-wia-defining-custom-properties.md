---
description: Definizione di proprietà personalizzate.
ms.assetid: 6adcf414-2c5a-451c-b30a-d1c161886c9a
title: Definizione di proprietà personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd91ee4d4e657ce0d6c01330d85e8df4ef57a36d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312446"
---
# <a name="defining-custom-properties"></a>Definizione di proprietà personalizzate

**Definizione di proprietà personalizzate**.

Se è necessario che Windows Image Acquisition (WIA) minidriver per definire proprietà personalizzate, è necessario usare la \_ \_ Proprietà DEVPROP privata WIA per le proprietà dell'elemento radice personalizzato e la proprietà ITEMPROP (WIA privato) per le proprietà degli \_ \_ elementi. Queste costanti sono definite in *wiadef. h*.

Nell'esempio di codice riportato di seguito vengono illustrate le definizioni per tre proprietà elemento radice. L'ID di proprietà della prima proprietà dell'elemento radice personalizzato, \_ ovvero la radice personalizzata \_ \_ 1, è definito in termini \_ di \_ DEVPROP privato WIA. Gli ID proprietà per ulteriori proprietà elemento radice sono definiti in termini di WIA \_ privato \_ DEVPROP + 1, WIA \_ privato \_ DEVPROP + 2 e così via. Il modello può essere continuato se sono necessarie proprietà aggiuntive dell'elemento radice personalizzato.


```
#define CUSTOM_ROOT_PROP_1 WIA_PRIVATE_DEVPROP
#define CUSTOM_ROOT_PROP_2 (WIA_PRIVATE_DEVPROP + 1) 
#define CUSTOM_ROOT_PROP_3 (WIA_PRIVATE_DEVPROP + 2)
```



Nell'esempio seguente vengono illustrate le definizioni per tre proprietà e ID di proprietà degli elementi figlio personalizzati. L'ID di proprietà per la prima proprietà elemento figlio personalizzato, l'elemento personalizzato \_ figlio \_ prop \_ 1, viene definito in termini di \_ ITEMPROP privato WIA \_ . Gli ID di proprietà per le proprietà aggiuntive degli elementi figlio sono definiti in termini di WIA \_ privato \_ ITEMPROP + 1 e così via. Come in precedenza, il modello può essere continuato se sono necessarie più proprietà di elemento figlio personalizzate.


```
#define CUSTOM_CHILD_PROP_1 WIA_PRIVATE_ITEMPROP
#define CUSTOM_CHILD_PROP_2 (WIA_PRIVATE_ITEMPROP + 1)
#define CUSTOM_CHILD_PROP_3 (WIA_PRIVATE_ITEMPROP + 2)
```



Per le proprietà WIA personalizzate è necessario che i nomi delle proprietà personalizzate siano associati agli ID delle proprietà personalizzate. Il codice di esempio seguente mostra le definizioni per tre nomi di proprietà dell'elemento radice personalizzato. Questi nomi di proprietà vengono usati con gli ID di proprietà personalizzati creati in un esempio precedente, in cui il nome della proprietà personalizzata contenuto in CUSTOM \_ \_La radice Prop \_ 1 \_ str è associata alla proprietà dell'elemento radice personalizzato ID della radice personalizzata \_ \_ prop \_ 1.


```
#define CUSTOM_ROOT_PROP_1_STR L"My First Custom Root Item Property"
#define CUSTOM_ROOT_PROP_2_STR L"My Second Custom Root Item Property"
#define CUSTOM_ROOT_PROP_3_STR L"My Third Custom Root Item Property"
```



> [!Note]  
> I nomi di proprietà WIA *non* sono localizzati in più lingue. Ciò è dovuto al fatto che le proprietà WIA possono essere lette dalle applicazioni utilizzando l'ID proprietà o il nome della proprietà. Se il nome viene usato, deve essere una costante, proprio come l'ID della proprietà.

 

 

 



