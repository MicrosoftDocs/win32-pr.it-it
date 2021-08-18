---
description: I moduli di uscita ricevono notifiche dal motore del server quando si verificano operazioni come il rilascio di un certificato.
ms.assetid: 5e7ee1f4-7e07-4a08-8e72-89b449804bc2
title: Uscire dai moduli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38ba8d821900ece1a4ce3eb3fcb2cc805d87274b451a3d5c8948d1e86ebf3547
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140754"
---
# <a name="exit-modules"></a>Uscire dai moduli

I moduli di uscita ricevono notifiche dal motore del server quando si verificano operazioni come il rilascio di un certificato. Un modulo di uscita viene implementato come [*libreria a collegamento dinamico*](../secgloss/d-gly.md) (DLL). Un'operazione tipica per un modulo di uscita è la pubblicazione di un certificato completato in un [](../secgloss/c-gly.md) percorso specificato (il modulo di uscita dell'autorità di certificazione globale (enterprise) predefinito, ad esempio, pubblica i certificati utente e gli elenchi di revoche di certificati (CRL) in Active Directory. Un modulo di uscita può usare [**l'interfaccia ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) per comunicare con Servizi certificati. Servizi certificati comunica con un modulo di uscita tramite chiamate COM dirette o, se il modulo non supporta le chiamate COM dirette, tramite Automazione.

Un modulo di uscita può visualizzare le proprietà e le estensioni del certificato esistenti e anche gli attributi e le proprietà della richiesta. Un modulo di uscita, tuttavia, non può modificare alcuna proprietà.

Servizi certificati fornisce un modulo di uscita predefinito, ma è anche possibile creare moduli di uscita personalizzati per soddisfare esigenze speciali. Tuttavia, prima di scrivere un modulo di uscita personalizzato, è consigliabile usare il modulo di uscita predefinito. Inoltre, per un'autorità di certificazione globale (enterprise), è consigliabile usare sempre il modulo di uscita predefinito, anche se è possibile aggiungere altri moduli di uscita personalizzati. Per altre informazioni, vedere [Scrittura di moduli di uscita personalizzati.](writing-custom-exit-modules.md)

 

 
