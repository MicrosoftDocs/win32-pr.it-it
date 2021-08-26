---
description: Panoramica della registrazione degli errori
ms.assetid: 1037f354-0415-4a5c-a96c-20ae714981af
title: Panoramica della registrazione degli errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcde3e0366ffca12dfcb5674259273ba1bbf25c1feed9be3ead57fa64cc42dc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904631"
---
# <a name="overview-of-error-logging"></a>Panoramica della registrazione degli errori

\[Questa API non è supportata e potrebbe essere modificata o non disponibile in futuro.\]

Per offrire alle applicazioni la massima flessibilità nella gestione degli errori, [DirectShow servizi di modifica](directshow-editing-services.md) usa un meccanismo di callback. L'applicazione implementa un metodo per la registrazione di un errore. In fase di esecuzione, se si verifica un errore, DES chiama il metodo fornito. Il metodo accetta parametri che descrivono l'errore. L'operazione che il metodo esegue con queste informazioni è l'utente. Dovrebbe tuttavia restituire il più rapidamente possibile o interferire con l'esecuzione del programma.

Il metodo di callback di registrazione degli errori è contenuto in un'interfaccia COM, [**IAMErrorLog.**](iamerrorlog.md) L'applicazione deve implementare questa interfaccia. Come tutte le interfacce COM, **IAMErrorLog** eredita **l'interfaccia IUnknown,** quindi anche l'applicazione deve implementarla.

Sono disponibili diverse opzioni per l'implementazione di queste interfacce COM. È possibile usare Active Template Library (ATL), che fornisce implementazioni di base dei **metodi IUnknown.** DirectShow fornisce anche una classe di base C++, [**CUnknown,**](cunknown.md)che semplifica l'implementazione di un'interfaccia COM. Per informazioni **sull'uso di CUnknown,** vedere [Come implementare IUnknown.](how-to-implement-iunknown.md)

Il codice di esempio in questo articolo definisce una classe C++ autonoma, che implementa sia **IUnknown** che **IAMErrorLog.** Il risultato non è un vero oggetto COM, perché non supporta **CoCreateInstance.** Tuttavia, questo approccio è adeguato ai fini dell'esempio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Errori di registrazione](logging-errors.md)
</dt> </dl>

 

 



