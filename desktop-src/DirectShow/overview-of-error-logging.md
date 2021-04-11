---
description: Panoramica della registrazione degli errori
ms.assetid: 1037f354-0415-4a5c-a96c-20ae714981af
title: Panoramica della registrazione degli errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4af82c35cdb34a238e280641015407c7a5d6f837
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124368"
---
# <a name="overview-of-error-logging"></a>Panoramica della registrazione degli errori

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Per garantire la massima flessibilità per le applicazioni nella gestione degli errori, i [servizi di modifica DirectShow](directshow-editing-services.md) utilizzano un meccanismo di callback. L'applicazione implementa un metodo per la registrazione di un errore. In fase di esecuzione, se si verifica un errore, DES chiama il metodo fornito. Il metodo accetta parametri che descrivono l'errore. L'operazione eseguita dal metodo con queste informazioni dipende dall'utente. (Deve essere restituito il più rapidamente possibile, tuttavia, oppure potrebbe interferire con l'esecuzione del programma).

Il metodo di callback per la registrazione degli errori è contenuto in un'interfaccia COM, [**IAMErrorLog**](iamerrorlog.md). L'applicazione deve implementare questa interfaccia. Come tutte le interfacce COM, **IAMErrorLog** eredita l'interfaccia **IUnknown** , quindi l'applicazione deve implementare anche tale interfaccia.

Sono disponibili diverse opzioni per l'implementazione di queste interfacce COM. È possibile utilizzare il Active Template Library (ATL), che fornisce le implementazioni predefinite dei metodi **IUnknown** . DirectShow fornisce anche una classe base C++, [**CUnknown**](cunknown.md), che semplifica l'implementazione di un'interfaccia com. Per informazioni sull'uso di **CUnknown**, vedere [How to implement IUnknown](how-to-implement-iunknown.md).

Il codice di esempio in questo articolo definisce una classe C++ autonoma che implementa sia **IUnknown** che **IAMErrorLog**. Il risultato non è un vero oggetto COM, perché non supporta **CoCreateInstance**. Tuttavia, questo approccio è adeguato ai fini dell'esempio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Errori di registrazione](logging-errors.md)
</dt> </dl>

 

 



