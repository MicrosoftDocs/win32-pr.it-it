---
description: Il writer di Active Directory non richiede azioni speciali durante le operazioni di backup.
ms.assetid: 66efd5e5-e6c9-4179-b119-1b5b977b0f9f
title: Backup e ripristino vss di Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e8312e974d705cd193eaaecdaa163a2d408836aedfb14c21ff97f72486efbf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751484"
---
# <a name="vss-backup-and-restore-of-the-active-directory"></a>Backup e ripristino vss di Active Directory

Il writer di Active Directory non richiede azioni speciali durante le operazioni di backup. Il writer fornirà al richiedente le informazioni sul componente e sul set di file e il richiedente usa queste informazioni per decidere quali file copiare nei supporti di backup. Non è necessario usare API speciali per eseguire il backup di Active Directory.

La modalità di esecuzione di un ripristino varia a seconda che Active Directory sia ripristinato come parte di un'operazione di ripristino di emergenza o se il ripristino si trova in un sistema in cui è in esecuzione Active Directory. Inoltre, la durata della copia di backup dello stato di Active Directory può essere un problema a causa di rimozione definitiva di Active Directory.

## <a name="active-directory-restoration-following-disaster-recovery"></a>Ripristino di Active Directory dopo il ripristino di emergenza

In seguito a un arresto anomalo che richiede il ripristino di emergenza, è possibile ripristinare Active Directory come parte del ripristino dello stato del sistema operativo.

Questa operazione di ripristino è essenzialmente un ripristino senza writer.

## <a name="active-directory-restoration-on-the-system-where-it-is-running"></a>Ripristino di Active Directory nel sistema in cui è in esecuzione

Il sistema deve essere riavviato in modalità ripristino servizi directory se Active Directory è attualmente in esecuzione nel server.

Il sistema operativo verrà quindi eseguito senza Active Directory e tutte le convalide degli utenti vengono eseguite tramite Gestione account di sicurezza (SAM) nel Registro di sistema. Solo l'amministratore è autorizzato a ripristinare Active Directory.

Una volta attivata la modalità ripristino servizio directory, un ripristino vss può procedere normalmente. Non esiste alcun motivo per usare API Di Active Directory Win32 non VSS per ripristinare lo stato di Active Directory.

## <a name="active-directory-restores-and-active-directory-tombstones"></a>Ripristini di Active Directory e rimozione definitiva di Active Directory

Qualsiasi piano di ripristino deve garantire che la durata del backup non superi la durata di rimozione definitiva di Active Directory (il valore predefinito è 60 giorni).

Il ripristino di un backup precedente all'operazione di rimozione definitiva causerà la creazione di oggetti che non vengono replicati in altri server in un controller di dominio.

Gli oggetti che non vengono replicati non verranno eliminati automaticamente nel controller di dominio (ripristinato) perché le rimozione definitiva di tali oggetti nelle altre repliche sono già state eliminate.

Un amministratore dovrà eliminare manualmente tutti gli oggetti nel controller di dominio ripristinato che non vengono replicati. I backup incrementali di Active Directory non sono supportati. È necessario un backup completo.

 

 



