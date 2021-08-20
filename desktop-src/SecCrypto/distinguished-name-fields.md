---
description: Contiene informazioni che devono identificare in modo univoco l'utente che effettua la richiesta.
ms.assetid: f0cc0e1b-370e-4548-97fe-8f6a4005540b
title: Campi del nome distinto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10465a481c1efbaa9637979bb5bb82880451fbe43800b968a4c9fefc5fbc4a3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767266"
---
# <a name="distinguished-name-fields"></a>Campi del nome distinto

Una [*richiesta di certificato*](../secgloss/c-gly.md) contiene informazioni che devono identificare in modo univoco l'utente che effettua la richiesta.

Le richieste di certificati in formato PKCS 10 accettate da Servizi certificati contengono campi di identificazione definiti campi nome \# distinto (DN). Questi campi conterranno le informazioni immesse dall'utente quando una richiesta di certificato viene creata da Key Manager, [certificate enrollment control](certificate-enrollment-control.md)o altri mezzi.

Di seguito sono riportate alcune linee guida per il completamento dei campi DN in una richiesta di certificato.



| Campo               | Descrizione                                                                                                                                                                                                                                                                                                                                                      |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome comune         | Certificati utente: è necessario immettere il nome completo della persona. Certificati computer: è necessario immettere il percorso nome host* completo usato nelle ricerche DNS in cui verrà eseguito il server, ad esempio ***/**  *HostName*. _Esempio_* _.com_*).<br/>                                                                                                  |
| Organization        | Il nome specificato per il campo Organizzazione deve essere il nome legale dell'organizzazione registrato con l'autorità di città, stato o paese/area geografica appropriata. Il nome legale dell'organizzazione deve essere usato nel campo Organizzazione.                                                                                                      |
| Unità organizzativa | Il campo Unità organizzativa può essere usato per distinguere le diverse divisioni all'interno di un'organizzazione, ad esempio "Internet Security Unit" o "Human Resources". È consigliabile usare questo campo anche per specificare un valore DBA (Doing Business As...).                                                                                           |
| Località            | Il campo Locality indica la città in cui risiede l'organizzazione. Se l'organizzazione ha solo una posizione locale, grazie alla presenza di una licenza aziendale registrata con il City Clerk per la Città di City of City of City in the State of Cancelli, il campo Locality deve contenere La città.                                                                |
| State or Province   | Il campo Stato o Provincia specifica dove si trova fisicamente l'organizzazione. Se l'organizzazione è incorporata in Delaware ma ha un amministratore di database (Doing Business As...) in California, usare California. Il campo Stato o Provincia non deve essere un campo abbreviato. Ad esempio, "CA" non è un nome di stato valido. "California" è il nome dello stato appropriato. |
| Paese/Area geografica      | Lo standard [*X.500*](../secgloss/x-gly.md) Naming Scheme richiede un codice paese/area geografica di 2 caratteri. Il codice paese/area geografica per il Stati Uniti è US; il codice paese/area geografica per il Canada è CA.                                                                                                                          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà nome](name-properties.md)
</dt> </dl>

 

 
