---
description: Il writer di Active Directory non richiede azioni speciali durante le operazioni di backup.
ms.assetid: 66efd5e5-e6c9-4179-b119-1b5b977b0f9f
title: Backup e ripristino del servizio Copia Shadow del volume del Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d4441a05e06e67c23467887857a0f7bbcde73f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526292"
---
# <a name="vss-backup-and-restore-of-the-active-directory"></a>Backup e ripristino del servizio Copia Shadow del volume del Active Directory

Il writer di Active Directory non richiede azioni speciali durante le operazioni di backup. Il writer fornirà al richiedente il componente e le informazioni sui set di file e il richiedente utilizzerà tali informazioni per decidere quali file copiare nei supporti di backup. Non è necessario usare API speciali per eseguire il backup del Active Directory.

Il modo in cui viene eseguito un ripristino varia a seconda che il Active Directory venga ripristinato come parte di un'operazione di ripristino di emergenza o se il ripristino è a un sistema in cui è in esecuzione il Active Directory. Inoltre, l'età della copia di backup dello stato del Active Directory potrebbe essere un problema a causa di Active Directory oggetti contrassegnati per la rimozione definitiva.

## <a name="active-directory-restoration-following-disaster-recovery"></a>Ripristino di Active Directory dopo il ripristino di emergenza

In seguito a un arresto anomalo che richiede il ripristino di emergenza, è possibile ripristinare il Active Directory come parte del ripristino dello stato del sistema operativo.

Questa operazione di ripristino è essenzialmente un ripristino di scrittura.

## <a name="active-directory-restoration-on-the-system-where-it-is-running"></a>Active Directory il ripristino sul sistema in cui è in esecuzione

Il sistema deve essere riavviato in modalità ripristino servizi directory se il Active Directory è attualmente in esecuzione nel server.

Il sistema operativo verrà quindi eseguito senza il Active Directory e la convalida dell'utente viene eseguita tramite Gestione account di sicurezza (SAM) nel registro di sistema. Solo l'amministratore dispone dell'autorizzazione per recuperare il Active Directory.

Una volta in modalità ripristino servizio directory, un ripristino VSS può procedere normalmente. Non esiste alcun motivo per usare API Win32 non VSS Active Directory per ripristinare lo stato di Active Directory.

## <a name="active-directory-restores-and-active-directory-tombstones"></a>Active Directory ripristini e Active Directory oggetti contrassegnati per la rimozione definitiva

Qualsiasi piano di ripristino deve garantire che l'età del backup non superi la durata Active Directory rimozione definitiva (il valore predefinito è 60 giorni).

Il ripristino di un backup precedente alla rimozione definitiva determinerà l'esecuzione di oggetti che non vengono replicati negli altri server da parte di un controller di dominio.

Gli oggetti che non vengono replicati non verranno eliminati automaticamente nel controller di dominio (ripristinato), perché gli oggetti contrassegnati per la rimozione definitiva di tali oggetti sulle altre repliche sono già stati eliminati.

Un amministratore dovrà eliminare manualmente ogni oggetto sul controller di dominio ripristinato che non viene replicato. I backup incrementali della Active Directory non sono supportati. è necessario un backup completo.

 

 



