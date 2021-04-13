---
description: Contiene informazioni che identificano in modo univoco l'utente che effettua la richiesta.
ms.assetid: f0cc0e1b-370e-4548-97fe-8f6a4005540b
title: Campi del nome distinto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a03495d19608e29aa60f09954c96a10f6c3cde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529083"
---
# <a name="distinguished-name-fields"></a>Campi del nome distinto

Una [*richiesta di certificato*](../secgloss/c-gly.md) contiene informazioni che devono identificare in modo univoco la persona che effettua la richiesta.

\#Le richieste di certificato in formato PKCS 10 accettate dai servizi certificati contengono campi di identificazione definiti campi nome distinto (DN). Questi campi conterranno le informazioni che vengono inserite dall'utente quando viene creata una richiesta di certificato da Gestione chiavi, dal [controllo di registrazione dei certificati](certificate-enrollment-control.md)o da altri mezzi.

Di seguito sono riportate alcune linee guida per il completamento dei campi DN in una richiesta di certificato.



| Campo               | Descrizione                                                                                                                                                                                                                                                                                                                                                      |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome comune         | Certificati utente: immettere il nome completo della persona. Certificati del computer: è necessario immettere il percorso completo del *nome host * **/**  usato nelle ricerche DNS su cui verrà eseguito il server, ad esempio *hostname ***.** _Esempio_* _. com_*).<br/>                                                                                                  |
| Organization        | Il nome specificato per il campo dell'organizzazione deve essere il nome valido per l'organizzazione registrato con l'autorità di città, stato o paese appropriata. Il nome legale dell'organizzazione deve essere utilizzato nel campo organizzazione.                                                                                                      |
| Unità organizzativa | Il campo unità organizzativa può essere usato per distinguere tra diverse divisioni all'interno di un'organizzazione, ad esempio "unità di sicurezza Internet" o "risorse umane". È inoltre consigliabile utilizzare questo campo per specificare un valore DBA (che esegue il business come...).                                                                                           |
| Località            | Il campo Località indica la città in cui risiede l'organizzazione. Se l'organizzazione ha un solo locale, in virtù della presenza di una licenza aziendale registrata con il Clerk City per la città di Cambridge nello stato del Massachusetts, il campo località deve contenere Cambridge.                                                                |
| State or Province   | Il campo stato o provincia specifica dove si trova fisicamente l'organizzazione. Se l'organizzazione è incorporata in Delaware ma ha un amministratore di database (che lavora come...) in California, usare California. Il campo stato o provincia non deve essere un campo abbreviato. Ad esempio, "CA" non è un nome di stato valido. "California" è il nome di stato appropriato. |
| Paese/Area geografica      | Per lo standard di denominazione [*X. 500*](../secgloss/x-gly.md) è necessario un codice paese a due caratteri. Il codice paese/area geografica per la Stati Uniti è US; il codice paese/area geografica per il Canada è CA.                                                                                                                          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà nome](name-properties.md)
</dt> </dl>

 

 
