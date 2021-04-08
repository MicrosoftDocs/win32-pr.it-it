---
title: Nomi dell'entità servizio
description: Un nome dell'entità servizio (SPN) è un identificatore univoco di un'istanza del servizio.
ms.assetid: 54b02853-4097-4e37-b7a2-6b5cfd168ece
ms.tgt_platform: multiple
keywords:
- Nomi dell'entità servizio
- Nome SPN vedere nomi dell'entità servizio
- Active Directory nome entità servizio
- Active Directory nome entità servizio, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa34b7d90803a324faced7d67b56c0b6a1f13af
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103872250"
---
# <a name="service-principal-names"></a>Nomi dell'entità servizio

Un nome dell'entità servizio (SPN) è un identificatore univoco di un'istanza del servizio. Gli SPN vengono utilizzati dall' [autenticazione Kerberos](mutual-authentication-using-kerberos.md) per associare un'istanza del servizio a un account di accesso al servizio. Questo consente a un'applicazione client di richiedere che il servizio esegua l'autenticazione di un account anche se il client non ha il nome dell'account.

Se si installano più istanze di un servizio in computer distribuiti in una foresta, a ogni istanza deve essere associato un nome SPN distinto. Se i client possono usare più nomi per l'autenticazione, una determinata istanza di servizio può presentare più SPN. Un SPN, ad esempio, include sempre il nome del computer host in cui è in esecuzione l'istanza del servizio, pertanto un'istanza del servizio potrebbe registrare un nome SPN per ogni nome o alias del relativo host. Per ulteriori informazioni sul formato SPN e sulla composizione di un nome SPN univoco, vedere [formati dei nomi per nomi SPN univoci](name-formats-for-unique-spns.md).

Prima che il servizio di autenticazione Kerberos possa utilizzare un nome SPN per autenticare un servizio, è necessario che il nome SPN sia registrato nell'oggetto account utilizzato dall'istanza del servizio per l'accesso. Un determinato nome SPN può essere registrato in un solo account. Per i servizi Win32, un programma di installazione del servizio specifica l'account di accesso quando viene installata un'istanza del servizio. Il programma di installazione compone quindi i nomi SPN e li scrive come proprietà dell'oggetto account in Active Directory Domain Services. Se l'account di accesso di un'istanza del servizio viene modificato, è necessario registrare nuovamente i nomi SPN con il nuovo account. Per ulteriori informazioni, vedere [come un servizio registra i relativi nomi SPN](how-a-service-registers-its-spns.md).

Per connettersi a un servizio, un client individua un'istanza del servizio, compone un nome SPN per l'istanza, esegue la connessione al servizio e presenta il nome SPN al servizio per l'autenticazione. Per ulteriori informazioni, vedere [modalità di composizione del nome SPN di un servizio](how-clients-compose-a-serviceampaposs-spn.md)da parte dei client.

## <a name="in-this-section"></a>Contenuto della sezione

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[Formati dei nomi per nomi SPN univoci](name-formats-for-unique-spns.md)
</dt> <dt>

[Come un servizio compone i relativi nomi SPN](how-a-service-composes-its-spns.md)
</dt> <dt>

[Modalità di registrazione dei nomi SPN da un servizio](how-a-service-registers-its-spns.md)
</dt> <dt>

[Composizione del nome SPN di un servizio da parte dei client](how-clients-compose-a-serviceampaposs-spn.md)
</dt> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Che cos'è un nome SPN e perché prestare attenzione?](/archive/blogs/autz_auth_stuff/what-is-a-spn-and-why-should-you-care)
</dt> <dt>

[Autenticazione reciproca tramite Kerberos](mutual-authentication-using-kerberos.md)
</dt> </dl>

 

 