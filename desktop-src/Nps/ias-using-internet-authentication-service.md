---
title: Uso delle estensioni di Server dei criteri di rete
description: Informazioni sull'uso di NPS Extensions. Il servizio di autenticazione Internet (IAS) è stato rinominato Server dei criteri di rete.
ms.assetid: 3ee16279-7e11-4587-ae43-f0296b7e7594
ms.tgt_platform: multiple
keywords:
- Internet Authentication Service IAS , attività
- Servizio di autenticazione Internet IAS , tramite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db3590ed10ec77e57c86bfad3e0e0b1160e70a2d6fcc08abc911a14614543f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074301"
---
# <a name="using-nps-extensions"></a>Uso delle estensioni di Server dei criteri di rete

Il servizio di autenticazione Internet (IAS) è stato rinominato Server dei criteri di rete. Il contenuto di questo argomento si applica sia a IAS che a Server dei criteri di rete. In tutto il testo, Server dei criteri di rete viene usato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente indicate come IAS.

**Windows Server 2008 R2 e Windows Server 2008: **

Gli esempi DialIn e MapName estendono la funzionalità NPS.



| Esempio             | Descrizione                                                                                                                                                                                                     |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DialIn<br/>  | In questo esempio viene implementata una DLL di estensione RADIUS che controlla il bit di accesso per l'utente.<br/>                                                                                                              |
| MapName<br/> | Questa DLL di estensione di esempio cerca l'account designato in tutti i domini attendibili. In questo modo gli utenti di più domini possono essere autenticati senza che gli utenti devono specificare il nome di dominio.<br/> |



 

È possibile trovare il codice sorgente per le applicazioni di esempio MapName e DialIn nell'elenco seguente. *Percorso*, %Percorso di installazione%, indica la directory di installazione di base per i computer x64. Vedere anche [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/windows-8-sdk)per Windows 8 , Microsoft Windows Software Development Kit (SDK) e Download per lo sviluppo di app Windows [Store.](https://msdn.microsoft.com/windows/apps/br229516)

<dl> <dt>

Windows SDK per Windows 8
</dt> <dd>

Windows Server 2012

Collegamento di download: N/D

MapName: No

DialIn: No

Località: N/D

</dd> <dt>

Microsoft Windows Software Development Kit (SDK) per Windows 7 e .NET Framework 4.0
</dt> <dd>

Windows Server 2008 R2

Collegamento per il download: <https://www.microsoft.com/download/en/confirmation.aspx?id=8279>

MapName: Sì

DialIn: No

Percorso: %Install Path% \\ Microsoft SDKs \\ Windows \\ v7.1 \\ Samples \\ netds \\ ias

</dd> <dt>

Windows SDK
</dt> <dd>

Windows Server 2008

Collegamento per il download: <https://www.microsoft.com/download/details.aspx?id=5023>

MapName: Sì

DialIn: No

Percorso: %Install Path% \\ Microsoft SDKs \\ Windows \\ v6.1 \\ Samples \\ NetDs \\ IAS

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Download per sviluppatori](https://msdn.microsoft.com/windows/apps/br229516)
</dt> <dt>

[Windows SDK per Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk)
</dt> </dl>

 

 





