---
title: Nomi dell'entità servizio
description: Un nome dell'entità servizio (SPN) è un identificatore univoco di un'istanza del servizio.
ms.assetid: 54b02853-4097-4e37-b7a2-6b5cfd168ece
ms.tgt_platform: multiple
keywords:
- Nomi dell'entità servizio
- SPN Vedere nomi di entità servizio
- nome dell'entità servizio AD
- nome dell'entità servizio AD , informazioni su
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6639ade82f029a89cb378de20bb279348962c4a991899f95e7f1b06157cd7ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024819"
---
# <a name="service-principal-names"></a>Nomi dell'entità servizio

Un nome dell'entità servizio (SPN) è un identificatore univoco di un'istanza del servizio. I nomi SPN vengono usati [dall'autenticazione Kerberos](mutual-authentication-using-kerberos.md) per associare un'istanza del servizio a un account di accesso al servizio. Ciò consente a un'applicazione client di richiedere al servizio di autenticare un account anche se il client non ha il nome dell'account.

Se si installano più istanze di un servizio in computer distribuiti in una foresta, a ogni istanza deve essere associato un nome SPN distinto. Se i client possono usare più nomi per l'autenticazione, una determinata istanza di servizio può presentare più SPN. Ad esempio, un nome SPN include sempre il nome del computer host in cui è in esecuzione l'istanza del servizio, pertanto un'istanza del servizio potrebbe registrare un nome SPN per ogni nome o alias del relativo host. Per altre informazioni sul formato SPN e sulla composizione di un nome SPN univoco, vedere [Formati dei nomi SPN univoci.](name-formats-for-unique-spns.md)

Prima che il servizio di autenticazione Kerberos possa utilizzare un nome SPN per autenticare un servizio, è necessario registrare il nome SPN nell'oggetto account utilizzato dall'istanza del servizio per l'accesso. Un nome SPN specificato può essere registrato in un solo account. Per i servizi Win32, un programma di installazione del servizio specifica l'account di accesso quando viene installata un'istanza del servizio. Il programma di installazione compone quindi i nomi SPN e li scrive come proprietà dell'oggetto account in Active Directory Domain Services. Se l'account di accesso di un'istanza del servizio viene modificato, i nomi SPN devono essere registrati nuovamente con il nuovo account. Per altre informazioni, vedere [How a Service Registers its SPNNs](how-a-service-registers-its-spns.md).

Per connettersi a un servizio, un client individua un'istanza del servizio, compone un nome SPN per l'istanza, esegue la connessione al servizio e presenta il nome SPN al servizio per l'autenticazione. Per altre informazioni, vedere [Modalità di composizione del nome SPN](how-clients-compose-a-serviceampaposs-spn.md)di un servizio da parte dei client.

## <a name="in-this-section"></a>Contenuto della sezione

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[Formati dei nomi SPN univoci](name-formats-for-unique-spns.md)
</dt> <dt>

[Modalità di composizione dei nomi SPN di un servizio](how-a-service-composes-its-spns.md)
</dt> <dt>

[Modalità di registrazione dei nomi SPN di un servizio](how-a-service-registers-its-spns.md)
</dt> <dt>

[Composizione del nome SPN di un servizio da parte dei client](how-clients-compose-a-serviceampaposs-spn.md)
</dt> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Che cos'è un nome SPN e perché è importante?](/archive/blogs/autz_auth_stuff/what-is-a-spn-and-why-should-you-care)
</dt> <dt>

[Autenticazione reciproca tramite Kerberos](mutual-authentication-using-kerberos.md)
</dt> </dl>

 

 