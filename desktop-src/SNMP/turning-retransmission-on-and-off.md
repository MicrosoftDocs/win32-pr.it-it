---
title: Attivazione e disattivazione della ritrasmissione
description: Un'applicazione può impostare la modalità di ritrasmissione con una chiamata alla funzione SnmpSetRetransmitMode. La nuova modalità di ritrasmissione si applica alle chiamate successive alla funzione SnmpSendMsg.
ms.assetid: 0e167014-2703-4942-91f0-c60a5c0d8e12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24936bcc90ed0debf66eb9040334fff3bceee2ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297943"
---
# <a name="turning-retransmission-on-and-off"></a><span data-ttu-id="b2a66-104">Attivazione e disattivazione della ritrasmissione</span><span class="sxs-lookup"><span data-stu-id="b2a66-104">Turning Retransmission On and Off</span></span>

<span data-ttu-id="b2a66-105">Un'applicazione può impostare la modalità di ritrasmissione con una chiamata alla funzione [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) .</span><span class="sxs-lookup"><span data-stu-id="b2a66-105">An application can set the retransmission mode with a call to the [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) function.</span></span> <span data-ttu-id="b2a66-106">La nuova modalità di ritrasmissione si applica alle chiamate successive alla funzione [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) .</span><span class="sxs-lookup"><span data-stu-id="b2a66-106">The new retransmission mode applies to subsequent calls to the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function.</span></span>

<span data-ttu-id="b2a66-107">Quando l'applicazione chiama **SnmpSetRetransmitMode** con il valore della modalità di ritrasmissione snmpapi \_ on, l'implementazione di Microsoft WinSNMP inizia l'esecuzione dei criteri di ritrasmissione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b2a66-107">When the application calls **SnmpSetRetransmitMode** with the retransmission mode value SNMPAPI\_ON, the Microsoft WinSNMP implementation begins execution of the application's retransmission policy.</span></span> <span data-ttu-id="b2a66-108">La nuova modalità di ritrasmissione non influisce sui messaggi SNMP in attesa.</span><span class="sxs-lookup"><span data-stu-id="b2a66-108">The new retransmission mode does not affect outstanding SNMP messages.</span></span> <span data-ttu-id="b2a66-109">Un messaggio in attesa è uno senza risposta al momento in cui l'applicazione modifica la modalità di ritrasmissione.</span><span class="sxs-lookup"><span data-stu-id="b2a66-109">An outstanding message is one that has no response at the time the application changes the retransmission mode.</span></span>

<span data-ttu-id="b2a66-110">Quando l'applicazione WinSNMP chiama la funzione [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) con il valore della modalità di ritrasmissione snmpapi \_ off, l'implementazione interrompe l'esecuzione dei criteri di ritrasmissione.</span><span class="sxs-lookup"><span data-stu-id="b2a66-110">When the WinSNMP application calls the [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) function with the retransmission mode value SNMPAPI\_OFF, the implementation stops executing the retransmission policy.</span></span> <span data-ttu-id="b2a66-111">L'implementazione Annulla i tentativi di ritrasmissione per i messaggi SNMP in attesa.</span><span class="sxs-lookup"><span data-stu-id="b2a66-111">The implementation cancels retransmission attempts for outstanding SNMP messages.</span></span> <span data-ttu-id="b2a66-112">Ciò è dovuto al fatto che l'implementazione di non può gestire tutte le richieste e le operazioni SNMP in attesa, oltre alle nuove richieste, prima che un contatore di timeout dell'applicazione o di ripetizione segnali un evento.</span><span class="sxs-lookup"><span data-stu-id="b2a66-112">This is because it may not be possible for the implementation to handle all outstanding SNMP requests and operations plus new requests, before an application time-out or retry counter signals an event.</span></span>

 

 




