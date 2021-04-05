---
title: Attributi di tipo puntatore
description: Gli attributi seguenti specificano le caratteristiche dei puntatori.
ms.assetid: 310d0dfe-eef3-447e-89fb-40f620976d00
keywords:
- MIDL di IDL, attributi, tipo di puntatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71371fff80d541242fcdc41d6c8adcc93dcdb754
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714356"
---
# <a name="pointer-type-attributes"></a>Attributi di tipo puntatore

Gli attributi seguenti specificano le caratteristiche dei puntatori.



| Attributo                                   | Utilizzo                                                                                                                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ptr**](ptr.md)                          | Designa un puntatore come puntatore completo, con tutte le funzionalità di un puntatore del linguaggio C, incluso l'aliasing.                                                                                       |
| [**ref**](ref.md)                          | Designa il tipo più semplice di puntatore in MIDL, ovvero uno che fornisce semplicemente l'indirizzo di alcuni dati. I puntatori di riferimento non possono mai essere null.                                                             |
| [**unico**](unique.md)                    | Consente a un puntatore di essere null, ma non supporta l'aliasing.                                                                                                                                               |
| [**puntatore \_ predefinito**](pointer-default.md) | Applicato a un'interfaccia per specificare il tipo di puntatore predefinito per tutti i puntatori di tale interfaccia, ad eccezione dei puntatori di parametro di primo livello, che vengono automaticamente predefiniti per i puntatori [**ref**](ref.md) . |
| [**IID \_ è**](iid-is.md)                   | Fornisce l'identificatore di interfaccia dell'interfaccia COM che rappresenta l'oggetto dell'indicatore di misura.                                                                                                            |
| [**string**](string.md)                    | Specifica che il puntatore punta a una stringa.                                                                                                                                                       |



 

 

 




