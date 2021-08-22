---
description: I nomi DNS sono costituiti da uno o più componenti separati da un punto (ad esempio, msdn.microsoft.com).
ms.assetid: 7e083cb5-cf0a-4284-8b54-dac856910c44
title: Nomi di computer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8687d6d510247a2bbb2850e6a668a63f0108b2bc344ed161cb73e28d2b47eeaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885791"
---
# <a name="computer-names"></a>Nomi di computer

I nomi DNS sono costituiti da uno o più componenti separati da un punto (ad esempio, msdn.microsoft.com). Ogni componente può essere fino a 63 byte. Ogni nome può essere fino a 255 byte in totale. I nomi DNS sono rappresentati nel set di caratteri UTF-8 o in Unicode. Per il nome non è prevista distinzione tra maiuscole e minuscole. Per altre informazioni, vedere [**DnsValidateName.**](/windows/desktop/api/windns/nf-windns-dnsvalidatename)

Un computer viene identificato in modo univoco dal nome DNS completo, costituito dal nome host DNS e dal nome del dominio DNS a cui è assegnato. Per recuperare il nome DNS completo, il nome host DNS o il nome di dominio DNS di un computer, chiamare la [**funzione GetComputerNameEx.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) Per impostare il nome host DNS o il nome di dominio DNS di un computer, chiamare la [**funzione SetComputerNameEx.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setcomputernameexa) Le modifiche al nome non hanno effetto fino a quando l'utente non riavvia il computer.

I nomi NetBIOS sono costituiti da un massimo di 15 byte di caratteri OEM, tra cui lettere, cifre, trattini e punti. Alcuni caratteri sono specifici del set di caratteri. I nomi NetBIOS sono in genere rappresentati nel set di caratteri OEM. Il set di caratteri OEM dipende dalle impostazioni locali. Alcuni set di caratteri OEM rappresentano determinati caratteri come due byte. Per convenzione, i nomi NetBIOS sono rappresentati in maiuscolo, dove l'algoritmo di conversione da minuscolo a maiuscolo dipende dal set di caratteri OEM.

Le [**funzioni SetComputerNameEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setcomputernameexa) [**e GetComputerNameEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) possono anche impostare e recuperare il nome NetBIOS del computer. Per convenzione, il nome NetBIOS e il nome host DNS sono interdipendenti. Quando si modifica il nome DNS, viene aggiornato anche il nome NetBIOS. Il nome NetBIOS è la rappresentazione OEM del nome host DNS fino a un massimo di \_ caratteri COMPUTERNAME \_ LENGTH. Se si imposta un nome host DNS di più di MAX COMPUTERNAME LENGTH caratteri, il nome NetBIOS viene impostato su una versione troncata \_ \_ del nome host DNS. In caso contrario, l'intero nome host DNS viene convertito nel nome NetBIOS OEM. Avviso: se si modifica il nome NetBIOS in modo che non sia un mapping troncato del nome DNS, si interromperanno le applicazioni che usano funzioni come [**DnsHostnameToComputerName**](/windows/desktop/api/Winbase/nf-winbase-dnshostnametocomputernamea) che si basano su questa convenzione.

 

 
