---
title: Gestione hardware remota
description: Gestione hardware remota
ms.assetid: 0ea6d075-6154-4ab9-adcb-e599e5aee614
ms.tgt_platform: multiple
keywords:
- Gestione hardware remota
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68bbb470d513b49d2158865c4c42051cc16856ed
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727394"
---
# <a name="remote-hardware-management"></a>Gestione hardware remota

Gestione remota Windows gestione hardware è finalizzata a ridurre i costi di amministrazione IT complessivi fornendo il monitoraggio e il controllo dei componenti hardware remoti, soprattutto prima che il sistema venga avviato e dopo un errore del sistema operativo.

Original Equipment Manufacturer (OEM) ha sviluppato un'architettura comune per soddisfare le esigenze di gestione dell'hardware. Una parte importante di questa architettura è la [*Baseboard Management Controller*](windows-remote-management-glossary.md) (BMC). Un BMC è un dispositivo specializzato che monitora lo stato del computer server. Il BMC fornisce il controllo remoto dell'hardware del server, recupera i dati sullo stato e riceve le notifiche relative agli errori critici e ad altre modifiche dello stato hardware. Uno script o un'applicazione che monitora un server remoto può ottenere dati dal server [*in banda*](windows-remote-management-glossary.md), tramite il sistema operativo remoto o [*fuori banda*](windows-remote-management-glossary.md), direttamente dal BMC.

Un BMC include sensori che possono rilevare, ad esempio, quando il computer server è in stato di surriscaldamento o quando la tensione non è compresa nell'intervallo accettabile. Per definire l'architettura del BMC sono disponibili diversi standard. L' [*interfaccia di gestione piattaforma intelligente (IPMI)*](windows-remote-management-glossary.md) è uno degli standard usati di frequente. Tuttavia, nonostante lo standard IPMI, l'accesso di gestione all'hardware del server è proprietario e richiede l'uso di strumenti di gestione forniti dagli OEM. Inoltre, l'accesso remoto a un BMC viene fornito usando un protocollo wire (RMCP) specializzato, che include meccanismi di sicurezza non standard per l'autenticazione dell'accesso.

Il [provider IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) Microsoft e il driver IPMI consentono di ottenere dati BMC da computer server remoti tramite un provider WMI standard con [classi](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)WMI. Sebbene sia possibile scrivere uno script WMI normale che ottenga dati remoti tramite DCOM, in molti casi il metodo preferito per ottenere i dati IPMI è tramite l'utilità da riga di comando **WinRM** o l' [API di scripting WINRM](winrm-scripting-api.md) o l' [API WinRM C++](winrm-c---api.md). L'utilità WinRM e le API del servizio WinRM si basano sul protocollo WS-Management e possono ottenere dati IPMI dal computer locale o remoto senza usare DCOM.

Il BMC dispone anche di un database di eventi denominato registro eventi di sistema (SEL) che registra gli eventi nel computer monitorato. Non è possibile sottoscrivere che questi eventi vengano recapitati a uno script come è possibile con le classi di evento WMI. Tuttavia, è possibile utilizzare lo strumento da riga di comando Wecutil.exe per sottoscriverli. Per ulteriori informazioni sull'utilizzo di questo strumento, digitare **wecutil/?** al prompt dei comandi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Protocollo WS-Management](ws-management-protocol.md)
</dt> <dt>

[Informazioni su Gestione remota Windows](about-windows-remote-management.md)
</dt> </dl>

 

 