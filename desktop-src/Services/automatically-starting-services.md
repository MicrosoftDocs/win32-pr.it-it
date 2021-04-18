---
description: Durante l'avvio del sistema, SCM avvia tutti i servizi di avvio automatico e i servizi da cui dipendono. Se, ad esempio, un servizio di avvio automatico dipende da un servizio di avvio a richiesta, viene avviato automaticamente anche il servizio di avvio a richiesta.
ms.assetid: 8aa60e96-a35e-4670-832c-c045d0903618
title: Avvio automatico dei servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b2e7ef0c65e72ee21145891b6f9598117a7afe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306340"
---
# <a name="automatically-starting-services"></a>Avvio automatico dei servizi

Durante l'avvio del sistema, SCM avvia tutti i servizi di avvio automatico e i servizi da cui dipendono. Se, ad esempio, un servizio di avvio automatico dipende da un servizio di avvio a richiesta, viene avviato automaticamente anche il servizio di avvio a richiesta.

L'ordine di caricamento è determinato dai seguenti elementi:

1.  Ordine dei gruppi nell'elenco del gruppo di ordini di caricamento. Queste informazioni vengono archiviate nel valore **ServiceGroupOrder** nella seguente chiave del registro di sistema:

    **\_ \_ \\ Controllo CurrentControlSet del sistema del computer \\ locale \\ HKEY**

    Per specificare il gruppo di ordini di caricamento per un servizio, usare il parametro *lpLoadOrderGroup* della funzione [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) o [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) .

2.  Ordine dei servizi all'interno di un gruppo specificato nel vettore di ordine dei tag. Queste informazioni vengono archiviate nel valore **GroupOrderList** nella seguente chiave del registro di sistema:

    **\_ \_ \\ Controllo CurrentControlSet del sistema del computer \\ locale \\ HKEY**

3.  Le dipendenze elencate per ogni servizio.

Al termine dell'avvio, il sistema esegue il programma di verifica dell'avvio specificato dal valore **BootVerificationProgram** della chiave del registro di sistema seguente: **HKEY \_ Local \_ computer \\ System \\ CurrentControlSet \\ Control**.

Per impostazione predefinita, questo valore non è impostato. Il sistema segnala semplicemente che l'avvio ha avuto esito positivo dopo che il primo utente ha eseguito l'accesso. È possibile fornire un programma di verifica di avvio che controlla la presenza di problemi nel sistema e segnala lo stato di avvio a SCM tramite la funzione [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) .

Al termine dell'avvio, il sistema salva un clone del database nell'ultima configurazione (ultima) corretta. Il sistema può ripristinare questa copia del database se le modifiche apportate al database attivo provocano un errore del riavvio del sistema. Di seguito è riportata la chiave del registro di sistema per il database:

**HKEY \_ \_ servizi di controllo di sistema del computer locale \\ \\ *xxx* \\**

dove *xxx* è il valore salvato nel seguente valore del registro di **sistema: HKEY \_ Local \_ computer \\ System \\ Select \\ LastKnownGood**.

Se un servizio di avvio automatico con \_ errore critico del servizio \_ non viene avviato, il controllo SCM riavvia il computer utilizzando la configurazione ultima. Se la configurazione ultima è già in uso, l'avvio ha esito negativo.

Un servizio di avvio automatico può essere configurato come servizio di avvio automatico ritardato chiamando la funzione [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) con le \_ informazioni di \_ avvio automatico ritardato della configurazione del servizio \_ \_ \_ . Questa modifica viene applicata dopo l'avvio del sistema successivo. Per altre informazioni, vedere [**\_ informazioni sull' \_ \_ avvio automatico \_ ritardato del servizio**](/windows/desktop/api/Winsvc/ns-winsvc-service_delayed_auto_start_info).

 

 



