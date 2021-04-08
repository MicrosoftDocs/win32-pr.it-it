---
title: Panoramica dell'architettura SSPI
description: SSPI è un'interfaccia software.
ms.assetid: 2497afea-33dd-45ae-891b-bacf390ef338
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 910cef52def2f398606fd541b8ed170f7e216078
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047090"
---
# <a name="sspi-architectural-overview"></a>Panoramica dell'architettura SSPI

SSPI è un'interfaccia software. Le librerie di programmazione distribuite, ad esempio RPC, possono usarle per le comunicazioni autenticate. Uno o più moduli software forniscono le effettive funzionalità di autenticazione. Ogni modulo, denominato SSP (Security Support Provider), viene implementato come libreria a collegamento dinamico (DLL). Un SSP fornisce uno o più pacchetti di sicurezza.

Sono disponibili diversi SSP e pacchetti. Windows viene fornito con il pacchetto di sicurezza NTLM e il pacchetto di sicurezza del protocollo Kerberos di Microsoft. Inoltre, è possibile scegliere di installare il pacchetto di sicurezza SSL (Secure Socket Layer) o qualsiasi altro SSP compatibile con SSPI.

L'uso di SSPI garantisce che, indipendentemente dall'SSP selezionato, l'applicazione acceda alle funzionalità di autenticazione in modo uniforme. Questa funzionalità consente all'applicazione di ottenere una maggiore indipendenza dall'implementazione della rete rispetto a quella disponibile in passato.

Le applicazioni distribuite comunicano tramite l'interfaccia RPC. Il software RPC a sua volta accede alle funzionalità di autenticazione di un provider di servizi condivisi tramite SSPI.

Per ulteriori informazioni, vedere [SSPI](/windows/desktop/SecAuthN/sspi).

 

 