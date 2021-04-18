---
description: In questo argomento vengono descritti i concetti di alto livello dell'interfaccia di rete in Windows, inclusi i modi in cui è possibile identificarli nel codice e le relative proprietà.
ms.assetid: CB01B5ED-C9DB-410B-8C98-E30D9A680847
title: Interfacce di rete
ms.topic: article
ms.date: 06/29/2018
ms.openlocfilehash: cc31be6062469750049a676807c2f8da24f473f1
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/26/2021
ms.locfileid: "106334049"
---
# <a name="network-interfaces"></a>Interfacce di rete

In questo argomento vengono descritti i concetti di alto livello dell'interfaccia di rete in Windows, inclusi i modi in cui è possibile identificarli nel codice e le relative proprietà. 

> [!IMPORTANT]
> Questo argomento è destinato a un pubblico sviluppatore, sia per le applicazioni di rete desktop Windows che per i driver di rete in modalità kernel. Tuttavia, alcune delle informazioni qui presentate possono essere utili anche per gli amministratori di sistema che gestiscono le interfacce di rete tramite i cmdlet di PowerShell.

## <a name="overview"></a>Panoramica

Un' *interfaccia di rete* è il punto in cui due parti di apparecchiature di rete o livelli di protocollo si connettono. In genere, questo è rappresentato da una scheda di interfaccia di rete (NIC) fisica per la connessione tra un computer e una rete privata o pubblica. Tuttavia, può anche assumere il formato di un componente solo software, ad esempio l'interfaccia di loopback ( `127.0.0.1` per IPv4 o `::1` per IPv6).

Le interfacce di rete sono definite da Internet Engineering Task Force (IETF) in [RFC 2863](https://tools.ietf.org/html/rfc2863) e non devono essere definite da Windows. Per domande dettagliate sul significato degli identificatori di interfaccia di rete, ad esempio **ifindex**, vedere le definizioni di IETF. Nella parte restante di questo argomento vengono illustrati i dettagli di implementazione specifici di Windows.

## <a name="network-interface-identifiers-and-properties"></a>Identificatori e proprietà dell'interfaccia di rete

In Windows, un'interfaccia di rete può essere identificata in modi diversi. Alcuni di questi identificatori vengono usati per distinguere le interfacce di rete tra loro, ma non tutti gli identificatori sono ugualmente adatti a tale attività a causa delle diverse proprietà. In genere, le interfacce di rete sono identificate da un indirizzo di rete a componenti esterni. Ad esempio, può trattarsi di un ID di nodo e di un numero di porta o semplicemente di un ID di nodo univoco. 

Nel codice, un'interfaccia di rete può essere identificata in molti modi. La tabella seguente illustra in dettaglio i modi in cui è possibile identificare un'interfaccia di rete insieme alle proprietà associate. È consigliabile usare il GUID di interfaccia (**ifGuid**) per la programmazione a meno che un'API specifica non richieda un identificatore di interfaccia di rete diverso.

> [!NOTE]
> Nella tabella seguente, le celle **grassetto** rappresentano una proprietà auspicabile per i programmatori di rete.

| Identificatore | Dimensione | È univoco nel sistema | È univoco nel mondo | Stimabile | Verrà riciclato se la scheda di interfaccia di rete è stata rimossa | Resi permanente tra i riavvii | Gli utenti finali possono modificare in qualsiasi momento | I driver possono essere modificati in qualsiasi momento | Conoscenza generale degli utenti finali | È sempre presente |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **ifIndex** | **4 byte** | **Sì** | No | No | Sì | Nessun<sup>1</sup> | **No** | **No** | **Parte**<sup>2</sup> | **Sì** |
| **NetLuid** | **8 byte** | **Sì** | No | No | Sì | **Sì** | **No** | **No** | No | **Sì** |
| **ifGuid** | **16 byte** | **Sì** | In **genere**<sup>3</sup> | No | **No** | **Sì** | **No** | **No** | No | **Sì** |
| **ifAlias** | 514 byte | **Sì per NIC**<sup>4</sup> | No | A volte<sup>5</sup> | Sì | **Sì** | Sì | **No** | **Sì** | In **genere**<sup>4</sup> |
| **ifDescr** | 514 byte | In genere<sup>6</sup> | No | No | Sì | **Sì** | **No** | Sì | **Sì** | **Solito** |
| **ifPhysAddress (indirizzo MAC)**| da 0 a 32 byte | In genere, per NIC | **In genere, per NIC** | **Sì** | **Collegato all'hardware** | **Sì** | **No** | **No** | **Sì** | In **genere** <sup>7</sup> |
| **ID istanza PnP** | Fino a 400 byte | **Sì** | No | No | Sì | **Sì** | **No** | **No** | No | **In genere, per NIC**<sup>8</sup> |
| **Posizione PnP (numero slot PCI)** | Fino a 400 byte | **Sì** | No | **Sì** | Sì | **Sì** | **No** | **No** | Talvolta | A volte<sup>8, 9</sup> |

Note per la tabella precedente:

1. Non è garantito che **IfIndexes** sia stabile tra i riavvii, anche se ricevono spesso lo stesso valore dell'avvio precedente. Non è quindi consigliabile che i driver usino **ifindex** , eccetto laddove richiesto da un'API.
2. Alcuni `netsh` comandi accettano `ifIndex` , o `index` , come input. Di conseguenza, alcuni utenti amministratori hanno familiarità con la proprietà **ifindex** se utilizzano il `netsh` comando di frequente.
3. Se un computer viene clonato o è stato immaginato, alcuni GUID potrebbero essere uguali. Inoltre, alcune interfacce di rete speciali, ad esempio l'interfaccia Teredo incorporata, potrebbero avere lo stesso GUID in tutti i computer.
4. NetCfg impone che un **ifAlias** sia una stringa non vuota ed è univoco tra tutte le schede di rete. Il provider di interfaccia NDIS, tuttavia, non lo è. Tutelare, è possibile trovare interfacce di rete speciali con nomi duplicati o vuoti. Questa situazione si verifica in genere con i team LBFO.
5. Solo se il firmware supporta la denominazione del dispositivo coerente. Typcically, i server dispongono di questa funzionalità.
6. NetCfg assegna **ifDescrs** univoche a tutte le interfacce di rete. Tuttavia, i driver possono chiamare un'API per modificare il **ifDescr** in qualsiasi elemento, incluso un elemento che non è univoco. Questa operazione viene eseguita da alcuni pacchetti software di terze parti.
7. Non tutti i tipi di supporto hanno un "indirizzo MAC". Alcuni tunnel, ad esempio, non hanno questo concetto e annunciano semplicemente una matrice di byte di lunghezza zero come indirizzo di rete.
8. Presente solo nelle interfacce di rete supportate da un dispositivo PnP. Ad esempio, le interfacce di loopback, le interfacce di filtro del peso leggero, le interfacce fornite da un provider di interfacce NDIS e alcune schede di interfaccia di rete predefinite speciali non dispongono di dispositivi PnP che li eseguono.
9. Solo alcuni bus PnP supportano un ID posizione PnP. I bus PCI e USB incorporati fanno, ma non i dispositivi con enumerazione radice.

## <a name="visibility-to-developers"></a>Visibilità per gli sviluppatori

Nella tabella precedente, tutte le proprietà eccetto le proprietà Plug and Play (PnP) sono visibili alle app desktop in modalità utente e ai driver in modalità kernel tramite un'intestazione condivisa (Netioapi. h). Le proprietà PnP sono visibili tramite l'intestazione Devpkey. h e vengono usate sia dalle app desktop in modalità utente che dai driver in modalità kernel. Vedere ad esempio la documentazione di [DEVPKEY](/windows-hardware/drivers/install/devpkey-device-instanceid) .

L'API [Helper IP](/windows/desktop/IpHlp/ip-helper-start-page) è disponibile anche per le applicazioni desktop in modalità utente e i driver in modalità kernel.

La superficie dell'API UWP espone direttamente la proprietà [ifGuid](/uwp/api/windows.networking.connectivity.networkadapter.networkadapterid) . Tuttavia, gli sviluppatori di app UWP possono importare la funzione [**GetIfTable2**](/windows/desktop/api/netioapi/nf-netioapi-getiftable2) usando P/Invoke se sono necessari per accedere ad altre proprietà dell'interfaccia di rete.

## <a name="related-topics"></a>Argomenti correlati

Per le definizioni MIB (Management Information Base) per le interfacce di rete, vedere [RFC 2863](https://tools.ietf.org/html/rfc2863).

Per le interfacce di rete NDIS nei driver di rete, vedere [interfacce di rete NDIS](/windows-hardware/drivers/network/ndis-network-interfaces2).

Per informazioni di riferimento sull'API Netioapi. h, vedere [intestazione Netioapi. h](/windows/desktop/api/netioapi/).
