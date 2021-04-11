---
title: Larghezza di banda della rete
description: I trasferimenti in background utilizzano la larghezza di banda di rete inattiva per mantenere l'esperienza interattiva dell'utente con altre applicazioni di rete, ad esempio Internet Explorer.
ms.assetid: c0b92a33-7afc-4250-8549-54cc46013239
ms.topic: article
ms.date: 10/09/2018
ms.openlocfilehash: 39a38a0efd5f2caea432fc9d13f7a958b6bcd407
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046979"
---
# <a name="network-bandwidth"></a>Larghezza di banda della rete

I trasferimenti in background utilizzano la larghezza di banda di rete inattiva per mantenere l'esperienza interattiva dell'utente con altre applicazioni di rete, ad esempio i Web browser. BITS regola l'uso della larghezza di banda Man mano che l'utente aumenta o diminuisce l'uso della larghezza di banda. Si noti che BITS trasferisce comunque una piccola quantità di dati durante un utilizzo di rete elevato per garantire l'avanzamento dei processi BITS.

BITS monitora il traffico di rete nel dispositivo gateway Internet (IGD) o nella scheda di interfaccia di rete (NIC) del client e usa solo la parte inattiva della larghezza di banda di rete. BITS consente inoltre a [LEDBAT](https://blogs.technet.microsoft.com/networking/2018/07/25/ledbat/) su connessioni http di ridurre la congestione della rete.

Se BITS usa la scheda di interfaccia di rete per misurare il traffico e nel client non sono in esecuzione applicazioni di rete, BITS utilizzerà la maggior parte della larghezza di banda disponibile. Ciò non significa che la rete oltre il client sia inattiva; la rete potrebbe essere a piena capacità.

Questo può costituire un problema se il client dispone di una scheda di rete veloce, ma la connessione Internet completa viene eseguita tramite un collegamento lento, ad esempio un router DSL, perché i bit competono per la larghezza di banda completa anziché utilizzare solo la larghezza di banda disponibile sul collegamento lento; BITS non ha visibilità del traffico di rete oltre il client.

Un dispositivo gateway che supporta i contatori può eliminare questo problema perché BITS misura il traffico sul collegamento lento e usa la larghezza di banda in modo appropriato. Se il dispositivo non supporta i contatori, è possibile ridurre l'effetto di questo tipo di connessione, usando il criterio **MaxInternetBandwidth** per limitare la larghezza di banda utilizzata da BITS nel computer client. Per informazioni dettagliate, vedere [criteri di gruppo](group-policies.md).

Se il computer contiene più interfacce di rete, ad esempio un modem, una rete privata virtuale (VPN) e diverse schede di interfaccia di rete (NIC), BITS chiama la funzione helper IP, [**GetBestInterfaceEx**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getbestinterfaceex), per determinare l'interfaccia con la route migliore all'indirizzo IP specificato. BITS eseguirà quindi il monitoraggio dell'utilizzo della larghezza di banda su tale interfaccia.

## <a name="using-an-internet-gateway-device-igd-to-determine-usage"></a>Uso di un dispositivo gateway Internet (IGD) per determinare l'utilizzo

Per usare un dispositivo gateway, il dispositivo deve supportare i contatori di byte (il dispositivo deve rispondere alle azioni GetTotalBytesSent e GetTotalBytesReceived) ed è necessario abilitare Universal Plug and Play (UPnP).

BITS utilizzerà la scheda di interfaccia di rete se:

-   Il dispositivo gateway non supporta i contatori
-   UPnP non è abilitato
-   Il server si trova all'interno della stessa subnet
-   Il dispositivo gateway non restituisce i dati del contatore in meno di 200 cicli

Se l'utente usa un profilo di rete pubblico, il profilo deve consentire UPnP. Per impostazione predefinita, i profili di rete privato e di dominio consentono UPnP.

Se viene usata una connessione VPN, BITS usa il primo dispositivo restituito da UPnP.