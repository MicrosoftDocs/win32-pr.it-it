---
title: Uso delle estensioni NPS
description: Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS).
ms.assetid: 3ee16279-7e11-4587-ae43-f0296b7e7594
ms.tgt_platform: multiple
keywords:
- IAS servizio di autenticazione Internet, attività
- IAS servizio di autenticazione Internet, utilizzo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a1cc9f10c810ec9fe16618144db11686a1e2132
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2020
ms.locfileid: "104516681"
---
# <a name="using-nps-extensions"></a>Uso delle estensioni NPS

Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS). Il contenuto di questo argomento si applica sia a IAS che a NPS. In tutto il testo, NPS viene utilizzato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente indicate come IAS.

* * Windows Server 2008 R2 e Windows Server 2008: * *

Gli esempi dialin e MapName estendono la funzionalità NPS.



| Esempio             | Descrizione                                                                                                                                                                                                     |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DialIn<br/>  | Questo esempio implementa una DLL di estensione RADIUS che controlla il bit di connessione per l'utente.<br/>                                                                                                              |
| MapName<br/> | Questa DLL di estensione di esempio esegue la ricerca di tutti i domini trusted per l'account designato. Ciò consente di autenticare gli utenti di più domini senza che gli utenti debbano specificare il nome di dominio.<br/> |



 

È possibile trovare il codice sorgente per le applicazioni di esempio MapName e dialin nell'elenco seguente. *Percorso*,% percorso di installazione%, designa la directory di installazione di base per i computer x64. Vedere anche [Windows Software Development Kit (SDK) per Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk), Microsoft Windows Software Development Kit (SDK) e [download per lo sviluppo di applicazioni Windows Store](https://msdn.microsoft.com/windows/apps/br229516).

<dl> <dt>

Windows SDK per Windows 8
</dt> <dd>

Windows Server 2012

Collegamento di download: N/A

MapName: No

Dialin: No

Località: N/A

</dd> <dt>

Microsoft Windows Software Development Kit (SDK) per Windows 7 e .NET Framework 4,0
</dt> <dd>

Windows Server 2008 R2

Collegamento per il download: <https://www.microsoft.com/download/en/confirmation.aspx?id=8279>

MapName: Sì

Dialin: No

Percorso:% install path% \\ Microsoft SDK \\ Windows \\ v 7.1 \\ Samples \\ netds \\ IAS

</dd> <dt>

Windows SDK
</dt> <dd>

Windows Server 2008

Collegamento per il download: <https://www.microsoft.com/download/details.aspx?id=5023>

MapName: Sì

Dialin: No

Percorso:% install path% \\ Microsoft SDK \\ Windows \\ v 6.1 \\ Samples \\ NetDs \\ IAS

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Download per sviluppatori](https://msdn.microsoft.com/windows/apps/br229516)
</dt> <dt>

[Windows SDK per Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk)
</dt> </dl>

 

 





