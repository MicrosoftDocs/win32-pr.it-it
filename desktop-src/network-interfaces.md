---
description: Questo argomento descrive i concetti di interfaccia di rete di alto Windows, inclusi i modi in cui possono essere identificati nel codice e le relative proprietà.
ms.assetid: CB01B5ED-C9DB-410B-8C98-E30D9A680847
title: Interfacce di rete
ms.topic: article
ms.date: 06/29/2018
ms.openlocfilehash: d74c875b579a34464190ca039e0176b8c01bef671b0ea6c24581023a49988645
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825457"
---
# <a name="network-interfaces"></a>Interfacce di rete

Questo argomento descrive i concetti di interfaccia di rete di alto Windows, inclusi i modi in cui possono essere identificati nel codice e le relative proprietà. 

> [!IMPORTANT]
> Questo argomento è destinato a un pubblico di sviluppatori, sia per Windows di rete desktop che per i driver di rete in modalità kernel. Tuttavia, alcune delle informazioni presentate qui possono essere utili anche per gli amministratori di sistema che gestiscono le interfacce di rete tramite i cmdlet di PowerShell.

## <a name="overview"></a>Panoramica

*Un'interfaccia di* rete è il punto in cui si connettono due componenti di apparecchiature di rete o livelli di protocollo. In genere, è rappresentato da una scheda di interfaccia di rete (NIC) fisica per la connessione tra un computer e una rete privata o pubblica. Tuttavia, può anche assumere la forma di un componente solo software, ad esempio l'interfaccia di loopback ( `127.0.0.1` per IPv4 o `::1` per IPv6).

Le interfacce di rete sono definite dalla Internet Engineering Task Force (IETF) in [RFC 2863](https://tools.ietf.org/html/rfc2863) e non devono essere definite da Windows. Per domande dettagliate sul significato degli identificatori di interfaccia di rete, ad esempio **ifIndex**, vedere le relative definizioni di IETF. Il resto di questo argomento illustra Windows dettagli di implementazione specifici.

## <a name="network-interface-identifiers-and-properties"></a>Identificatori e proprietà dell'interfaccia di rete

In Windows, un'interfaccia di rete può essere identificata in modi diversi. Alcuni di questi identificatori vengono usati per distinguere le interfacce di rete l'una dall'altra, ma non tutti gli identificatori sono ugualmente adatti a tale attività a causa delle proprietà diverse. In genere, le interfacce di rete sono identificate da un indirizzo di rete per i componenti esterni. Ad esempio, può trattarsi di un ID nodo e di un numero di porta o semplicemente di un ID nodo univoco. 

Nel codice un'interfaccia di rete può essere identificata in molti modi. Nella tabella seguente vengono fornite informazioni dettagliate sulle modalità di identificazione di un'interfaccia di rete insieme alle proprietà associate. È consigliabile usare il GUID dell'interfaccia ( ifGuid ) per la **programmazione,** a meno che un'API specifica non richieda un identificatore di interfaccia di rete diverso.

> [!NOTE]
> Nella tabella seguente le celle **in grassetto** rappresentano una proprietà auspicabile per i programmatori di rete.

| Identificatore | Dimensione | È univoco nel sistema | È unico al mondo | È prevedibile | Verrà riciclato se la scheda di interfaccia di rete viene rimossa | Persiste tra i riavvii | Gli utenti finali possono modificare in qualsiasi momento | I driver possono modificare in qualsiasi momento | Familiarità generale con gli utenti finali | È sempre presente |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **ifIndex** | **4 byte** | **Sì** | No | No | Sì | N.<sup>1</sup> | **No** | **No** | **Circa**<sup>2</sup> | **Sì** |
| **NetLuid** | **8 byte** | **Sì** | No | No | Sì | **Sì** | **No** | **No** | No | **Sì** |
| **ifGuid** | **16 byte** | **Sì** | **In genere**<sup>3</sup> | No | **No** | **Sì** | **No** | **No** | No | **Sì** |
| **ifAlias** | 514 byte | **Sì per le schede di interfaccia di** rete <sup>4</sup> | No | A volte<sup>5</sup> | Sì | **Sì** | Sì | **No** | **Sì** | **In genere**<sup>4</sup> |
| **ifDescr** | 514 byte | In<sup>genere 6</sup> | No | No | Sì | **Sì** | **No** | Sì | **Sì** | **Solito** |
| **ifPhysAddress (INDIRIZZO MAC)**| Da 0 a 32 byte | In genere, per le schede di interfaccia di rete | **In genere, per le schede di interfaccia di rete** | **Sì** | **Associato all'hardware** | **Sì** | **No** | **No** | **Sì** | **In genere** <sup>7</sup> |
| **ID istanza PnP** | Fino a 400 byte | **Sì** | No | No | Sì | **Sì** | **No** | **No** | No | **In genere, per le schede di interfaccia di rete**<sup>8</sup> |
| **Posizione PnP (numero slot PCI)** | Fino a 400 byte | **Sì** | No | **Sì** | Sì | **Sì** | **No** | **No** | A volte | A<sup>volte 8,9</sup> |

Note per la tabella precedente:

1. **Non è garantito** che gli indici ifIndexes siano stabili tra un riavvio e l'altro, anche se spesso ricevono lo stesso valore dell'avvio precedente. Pertanto, non è consigliabile che i driver usino **ifIndex tranne** quando richiesto da un'API.
2. Alcuni `netsh` comandi `ifIndex` accettano , o come `index` input. Pertanto, alcuni utenti amministrativi hanno familiarità con la **proprietà ifIndex** se usano spesso `netsh` il comando.
3. Se un computer viene clonato o immagine, alcuni GUID potrebbero essere uguali. Inoltre, alcune interfacce di rete speciali, ad esempio l'interfaccia Teredo predefinita, potrebbero avere lo stesso GUID in tutti i computer.
4. NetCfg impone che **ifAlias** sia una stringa non vuota ed è univoco tra tutte le schede di interfaccia di rete. Tuttavia, il provider di interfaccia NDIS non lo fa. In questo caso, è possibile trovare interfacce di rete speciali con nomi duplicati o vuoti. Questo problema si verifica più comunemente con i team LBFO.
5. Solo se il firmware supporta la denominazione coerente dei dispositivi. Dal punto di vista tipografico, i server hanno questa funzionalità.
6. NetCfg assegna **ifDescrs univoco a** tutte le interfacce di rete. Tuttavia, i driver possono chiamare un'API per modificare **ifDescr** in qualsiasi elemento, incluso un elemento non univoco. A tale scopo, alcuni pacchetti software di terze parti.
7. Non tutti i tipi di supporti hanno un "indirizzo MAC". Ad esempio, alcuni tunnel non hanno questo concetto e annunciano semplicemente una matrice di byte di lunghezza zero come indirizzo di rete.
8. Presente solo nelle interfacce di rete supportate da un dispositivo PnP. Ad esempio, le interfacce di loopback, le interfacce di filtro leggere, le interfacce fornite da un provider di interfacce NDIS e alcune schede di interfaccia di rete speciali incorporate non dispongono di dispositivi PnP che le backup.
9. Solo alcuni bus PnP supportano un ID località PnP. I bus PCI e USB incorporati lo fanno, mentre i dispositivi con enumerazione radice non lo fanno.

## <a name="visibility-to-developers"></a>Visibilità per gli sviluppatori

Nella tabella precedente tutte le proprietà ad eccezione delle proprietà Plug and Play (PnP) sono visibili alle app desktop in modalità utente e ai driver in modalità kernel tramite un'intestazione condivisa (Netioapi.h). Le proprietà PnP sono visibili tramite l'intestazione Devpkey.h e vengono usate sia dalle app desktop in modalità utente che dai driver in modalità kernel. Ad esempio, vedere la [documentazione di DEVPKEY.](/windows-hardware/drivers/install/devpkey-device-instanceid)

[L'API helper IP](/windows/desktop/IpHlp/ip-helper-start-page) è disponibile anche per le app desktop in modalità utente e i driver in modalità kernel.

La superficie dell'API UWP espone direttamente solo la proprietà [ifGuid.](/uwp/api/windows.networking.connectivity.networkadapter.networkadapterid) Tuttavia, gli sviluppatori di app UWP possono importare la funzione [**GetIfTable2**](/windows/desktop/api/netioapi/nf-netioapi-getiftable2) usando P/Invoke se sono necessari per accedere ad altre proprietà dell'interfaccia di rete.

## <a name="related-topics"></a>Argomenti correlati

Per le definizioni MIB (Management Information Base) per le interfacce di rete, [vedere RFC 2863.](https://tools.ietf.org/html/rfc2863)

Per le interfacce di rete NDIS nei driver di rete, vedere [Interfacce di rete NDIS.](/windows-hardware/drivers/network/ndis-network-interfaces2)

Per informazioni di riferimento sull'API Netioapi.h, vedere intestazione [netioapi.h.](/windows/desktop/api/netioapi/)
