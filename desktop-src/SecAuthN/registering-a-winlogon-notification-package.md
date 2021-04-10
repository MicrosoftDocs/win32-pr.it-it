---
description: Le informazioni sui pacchetti di notifica di Winlogon sono memorizzate nel registro di sistema. Le voci del registro di sistema specificano il nome del pacchetto di notifica, il nome della DLL che implementa il pacchetto e i nomi delle funzioni che gestiscono gli eventi Winlogon.
ms.assetid: dbe8d5a3-8927-4b95-a1a0-82c8e12ba8c1
title: Registrazione di un pacchetto di notifica Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25b353220727c828a0fa0b1d6f9b479bfa54832e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227374"
---
# <a name="registering-a-winlogon-notification-package"></a>Registrazione di un pacchetto di notifica Winlogon

Le informazioni sui pacchetti di notifica di [*Winlogon*](../secgloss/w-gly.md) sono memorizzate nel registro di sistema. Le voci del registro di sistema specificano il nome del pacchetto di notifica, il nome della DLL che implementa il pacchetto e i nomi delle funzioni che gestiscono gli eventi Winlogon.

Quando si avvia Winlogon, viene verificato il registro di sistema e vengono caricati tutti i pacchetti di notifica registrati. Quando si verifica un evento, Winlogon chiama la funzione del gestore eventi designata per ogni pacchetto. È possibile registrare più pacchetti di notifiche degli eventi in un sistema.

Per registrare il pacchetto di notifica, creare una chiave del registro di sistema denominata **Notify** come sottochiave della chiave del registro di sistema seguente e aggiungere i valori descritti in dettaglio nelle [voci del registro](registry-entries.md)di sistema.

**HKEY \_ Software del \_ computer locale** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon**

 

 
