---
title: Creazione di un riferimento esterno
description: Se viene creato un oggetto crossRef esterno e un controller di dominio lo usa per generare un riferimento, l'oggetto crossRef fornisce due elementi dati importanti nelle proprietà seguenti.
ms.assetid: 9805390c-9e8d-4afd-bffc-43abf6055413
ms.tgt_platform: multiple
keywords:
- riferimenti esterni Active Directory
- Esempi di Active Directory Active Directory, creazione di un riferimento esterno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801a9306c374a0c22d206e9a0f9dbb8cd240da0c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724591"
---
# <a name="creating-an-external-referral"></a>Creazione di un riferimento esterno

Se viene creato un oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) esterno e un controller di dominio lo usa per generare un riferimento, l'oggetto **crossRef** fornisce due elementi dati importanti nelle proprietà seguenti. Per ulteriori informazioni sulle situazioni in cui questo può verificarsi, vedere la sezione precedente.



| Proprietà                           | Descrizione                                                                                                                                                         |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot) | Specifica il server o il dominio che può fornire dati dal contesto dei nomi specificato in [**NCName**](/windows/desktop/ADSchema/a-ncname).                                           |
| [**nCName**](/windows/desktop/ADSchema/a-ncname)   | Specifica il nome distinto per il dominio, lo schema o il contenitore di configurazione radice nel server o nel dominio specificato da [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot). |



 

Se, ad esempio, il server con indirizzo DNS di serv1.northwest.Fabrikam.com serve il contesto dei nomi radice in CN = MyServer, OU = MyDOM, O = Fabrikam, impostare [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot) sull'indirizzo DNS di tale server e [**NCName**](/windows/desktop/ADSchema/a-ncname) sul nome distinto del contenitore di dominio, schema o configurazione.

Per ulteriori informazioni e un esempio di codice in cui viene illustrato come creare un riferimento esterno, vedere il [codice di esempio per la creazione di un oggetto crossRef esterno](example-code-for-creating-an-external-crossref-object.md).

 

 