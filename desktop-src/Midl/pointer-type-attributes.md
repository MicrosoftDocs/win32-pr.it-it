---
title: Attributi del tipo di puntatore
description: Gli attributi seguenti specificano le caratteristiche dei puntatori.
ms.assetid: 310d0dfe-eef3-447e-89fb-40f620976d00
keywords:
- IDL MIDL , attributi, pointer-type
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb8355a71428c957804596531ea428fb99a779478b677eaa2094cc4db323c45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013729"
---
# <a name="pointer-type-attributes"></a>Attributi del tipo di puntatore

Gli attributi seguenti specificano le caratteristiche dei puntatori.



| Attributo                                   | Utilizzo                                                                                                                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ptr**](ptr.md)                          | Designa un puntatore come puntatore completo, con tutte le funzionalità di un puntatore del linguaggio C, incluso l'aliasing.                                                                                       |
| [**ref**](ref.md)                          | Designa il tipo più semplice di puntatore in MIDL, che fornisce semplicemente l'indirizzo di alcuni dati. I puntatori di riferimento non possono mai essere Null.                                                             |
| [**Unico**](unique.md)                    | Consente a un puntatore di essere Null, ma non supporta l'aliasing.                                                                                                                                               |
| [**impostazione predefinita del \_ puntatore**](pointer-default.md) | Applicato a un'interfaccia per specificare il tipo di puntatore predefinito per tutti i puntatori in tale interfaccia, ad eccezione dei puntatori di parametro di primo livello, che per impostazione predefinita vengono automaticamente puntatori [**di**](ref.md) riferimento. |
| [**iid \_ è**](iid-is.md)                   | Fornisce l'identificatore di interfaccia dell'interfaccia COM che è l'oggetto del puntatore.                                                                                                            |
| [**string**](string.md)                    | Specifica che il puntatore punta a una stringa.                                                                                                                                                       |



 

 

 




