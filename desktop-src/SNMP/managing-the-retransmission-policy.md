---
title: Gestione dei criteri di ritrasmissione
description: L'applicazione WinSNMP può richiedere che l'implementazione di Microsoft WinSNMP esegua i criteri di ritrasmissione dell'applicazione. Quando l'implementazione gestisce la ritrasmissione, usa il periodo di timeout e i valori del numero di tentativi nel database.
ms.assetid: 1f1a9589-3566-4d90-ac4d-7acf69f34676
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f2e47d983f8da62ccb8ffbe9c20b35c71bfbb70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045044"
---
# <a name="managing-the-retransmission-policy"></a><span data-ttu-id="c9623-104">Gestione dei criteri di ritrasmissione</span><span class="sxs-lookup"><span data-stu-id="c9623-104">Managing the Retransmission Policy</span></span>

<span data-ttu-id="c9623-105">L'applicazione WinSNMP può richiedere che l'implementazione di Microsoft WinSNMP esegua i criteri di ritrasmissione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c9623-105">The WinSNMP application can request that the Microsoft WinSNMP implementation execute the application's retransmission policy.</span></span> <span data-ttu-id="c9623-106">Quando l'implementazione gestisce la ritrasmissione, usa il periodo di timeout e i valori del numero di tentativi nel database.</span><span class="sxs-lookup"><span data-stu-id="c9623-106">When the implementation manages retransmission, it uses the time-out period and the retry count values in its database.</span></span>

<span data-ttu-id="c9623-107">L'implementazione identifica la modalità di ritrasmissione predefinita in un valore restituito dalla funzione [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) durante l'inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="c9623-107">The implementation identifies the default retransmission mode in a return value from the [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) function during initialization.</span></span> <span data-ttu-id="c9623-108">La modalità può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="c9623-108">The mode can be one of the following values.</span></span>



| <span data-ttu-id="c9623-109">Valore</span><span class="sxs-lookup"><span data-stu-id="c9623-109">Value</span></span>        | <span data-ttu-id="c9623-110">Significato</span><span class="sxs-lookup"><span data-stu-id="c9623-110">Meaning</span></span>                                                                      |
|--------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c9623-111">SNMPAPI \_</span><span class="sxs-lookup"><span data-stu-id="c9623-111">SNMPAPI\_ON</span></span>  | <span data-ttu-id="c9623-112">L'implementazione sta eseguendo i criteri di ritrasmissione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c9623-112">The implementation is executing the application's retransmission policy.</span></span>     |
| <span data-ttu-id="c9623-113">SNMPAPI \_ disattivato</span><span class="sxs-lookup"><span data-stu-id="c9623-113">SNMPAPI\_OFF</span></span> | <span data-ttu-id="c9623-114">L'implementazione non esegue i criteri di ritrasmissione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c9623-114">The implementation is not executing the application's retransmission policy.</span></span> |



 

<span data-ttu-id="c9623-115">Un'applicazione WinSNMP può recuperare in qualsiasi momento la modalità di ritrasmissione corrente attiva per l'implementazione chiamando la funzione [**SnmpGetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode) .</span><span class="sxs-lookup"><span data-stu-id="c9623-115">A WinSNMP application can retrieve at any time the current retransmission mode in effect for the implementation by calling the [**SnmpGetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode) function.</span></span> <span data-ttu-id="c9623-116">L'API WinSNMP fornisce altre [funzioni di database](winsnmp-functions.md) che semplificano la gestione dei criteri di ritrasmissione.</span><span class="sxs-lookup"><span data-stu-id="c9623-116">The WinSNMP API provides other [database functions](winsnmp-functions.md) that simplify management of the retransmission policy.</span></span>

<span data-ttu-id="c9623-117">In qualsiasi momento durante l'esecuzione del programma, l'applicazione WinSNMP può regolare l'esecuzione dei criteri eseguendo uno dei passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="c9623-117">At any time during program execution, the WinSNMP application can adjust execution of the policy by performing one of the following steps:</span></span>

-   <span data-ttu-id="c9623-118">Richiedere che l'implementazione avvii o arresti l'esecuzione dei criteri di ritrasmissione chiamando la funzione [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) .</span><span class="sxs-lookup"><span data-stu-id="c9623-118">Request that the implementation start or stop executing the retransmission policy by calling the [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) function.</span></span> <span data-ttu-id="c9623-119">Per ulteriori informazioni, vedere [attivazione e disattivazione della ritrasmissione](turning-retransmission-on-and-off.md).</span><span class="sxs-lookup"><span data-stu-id="c9623-119">For more information, see [Turning Retransmission On and Off](turning-retransmission-on-and-off.md).</span></span>
-   <span data-ttu-id="c9623-120">Modificare il periodo di timeout e i valori del numero di tentativi nel database di implementazione.</span><span class="sxs-lookup"><span data-stu-id="c9623-120">Modify the time-out period and retry count values in the implementation's database.</span></span> <span data-ttu-id="c9623-121">Per ulteriori informazioni, vedere [modifica del criterio di ritrasmissione](changing-the-retransmission-policy.md).</span><span class="sxs-lookup"><span data-stu-id="c9623-121">For more information, see [Changing the Retransmission Policy](changing-the-retransmission-policy.md).</span></span>
-   <span data-ttu-id="c9623-122">Chiamare la funzione [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) per annullare il ciclo di ritrasmissione e rilasciare le strutture di dati interne associate a una singola richiesta di messaggio SNMP.</span><span class="sxs-lookup"><span data-stu-id="c9623-122">Call the [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) function to cancel the retransmission cycle and release internal data structures associated with a single SNMP message request.</span></span> <span data-ttu-id="c9623-123">Per ulteriori informazioni, vedere [annullamento della ritrasmissione](canceling-retransmission.md).</span><span class="sxs-lookup"><span data-stu-id="c9623-123">For more information, see [Canceling Retransmission](canceling-retransmission.md).</span></span>

<span data-ttu-id="c9623-124">L'applicazione può eseguire i propri criteri di ritrasmissione.</span><span class="sxs-lookup"><span data-stu-id="c9623-124">The application can execute its own retransmission policy.</span></span> <span data-ttu-id="c9623-125">In questo caso, l'esecuzione può essere basata sui valori nel database.</span><span class="sxs-lookup"><span data-stu-id="c9623-125">In this case, execution may or may not be based on the values in the database.</span></span>

 

 




