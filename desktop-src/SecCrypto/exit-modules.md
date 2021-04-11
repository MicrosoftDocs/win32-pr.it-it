---
description: I moduli di uscita ricevono notifiche dal motore del server quando si verificano operazioni quali l'emissione di un certificato.
ms.assetid: 5e7ee1f4-7e07-4a08-8e72-89b449804bc2
title: Moduli di uscita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5fc0668717c4a7a690cce8a03ff8c140333347b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232655"
---
# <a name="exit-modules"></a>Moduli di uscita

I moduli di uscita ricevono notifiche dal motore del server quando si verificano operazioni quali l'emissione di un certificato. Un modulo di uscita viene implementato come [*libreria a collegamento dinamico*](../secgloss/d-gly.md) (dll). Un'operazione tipica per un modulo di uscita consiste nel pubblicare un certificato completato in un percorso specificato (il modulo di uscita dell'autorità di certificazione globale (Enterprise), ad esempio, pubblica i certificati utente e gli [*elenchi di revoche di certificati*](../secgloss/c-gly.md) (CRL) nel Active Directory). Un modulo di uscita può usare l'interfaccia [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) per comunicare con i servizi certificati. Servizi certificati comunica con un modulo di uscita per mezzo di chiamate COM dirette o, se il modulo non supporta le chiamate COM dirette, per mezzo dell'automazione.

Un modulo di uscita può visualizzare le estensioni e le proprietà del certificato esistenti e può anche visualizzare gli attributi e le proprietà della richiesta. Un modulo di uscita, tuttavia, non può modificare alcuna proprietà.

Servizi certificati fornisce un modulo di uscita predefinito, ma è anche possibile creare moduli di uscita personalizzati per soddisfare esigenze specifiche. Tuttavia, prima di scrivere un modulo di uscita personalizzato, provare a usare il modulo di uscita predefinito. Inoltre, per un'autorità di certificazione dell'organizzazione (Enterprise), è necessario usare sempre il modulo di uscita predefinito, anche se è possibile aggiungere altri moduli di uscita personalizzati. Per altre informazioni, vedere [scrittura di moduli di uscita personalizzati](writing-custom-exit-modules.md).

 

 
