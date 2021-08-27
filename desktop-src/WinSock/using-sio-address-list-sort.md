---
description: SIO ADDRESS LIST SORT IOCTL consente agli sviluppatori di applicazioni di ordinare un elenco di indirizzi di destinazione \_ IPv6 e IPv4 per determinare l'indirizzo migliore disponibile per stabilire \_ \_ una connessione. SIO \_ ADDRESS \_ LIST SORT \_ IOCTL è supportato in Windows XP e versioni successive.
ms.assetid: bf380ddf-8171-4ef4-be47-94c7a6aabf0a
title: Uso di SIO_ADDRESS_LIST_SORT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0bce27088052bfc029047d5f498ad90962567b50015a5331b26016e455d770
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121146"
---
# <a name="using-sio_address_list_sort"></a>Uso di SIO \_ ADDRESS \_ LIST \_ SORT

**SIO \_ ADDRESS \_ LIST \_ SORT** IOCTL consente agli sviluppatori di applicazioni di ordinare un elenco di indirizzi di destinazione IPv6 e IPv4 per determinare l'indirizzo migliore disponibile per stabilire una connessione. **SIO \_ ADDRESS \_ LIST \_ SORT** IOCTL è supportato in Windows XP e versioni successive.

In Windows Vista e versioni successive la funzione [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) accetta un elenco fornito di potenziali indirizzi IP di destinazione, associa gli indirizzi di destinazione agli indirizzi IP locali del computer host e ordina le coppie in base alla coppia di indirizzi più adatta per la comunicazione tra i due peer. È consigliabile usare la funzione **CreateSortedAddressPairs** invece di **SIO \_ ADDRESS LIST \_ \_ SORT** IOCTL Windows Vista e versioni successive.

Nelle sezioni seguenti vengono descritte le considerazioni **sull'utilizzo di SIO \_ ADDRESS \_ LIST \_ SORT.**

## <a name="parameters"></a>Parametri

Il buffer passato a **SIO \_ ADDRESS LIST \_ \_ SORT** è una [**struttura SOCKET ADDRESS \_ \_ LIST.**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) Ogni [**INDIRIZZO \_ SOCKET**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) nell'elenco deve essere in formato SOCKADDR \_ IN6.

**L'IOCTL SIO \_ ADDRESS \_ LIST \_ SORT** ordina sia gli indirizzi IPv6 che IPv4 Windows Vista e versioni successive. Tutti gli indirizzi IPv4 nell'elenco da ordinare devono essere nel formato di indirizzo IPv6 mappato a IPv4. Per altre informazioni sul formato di indirizzo IPv6 mappato a IPv4, vedere [Dual-Stack Sockets](dual-stack-sockets.md).

In Windows Server 2003 e Windows XP, **SIO \_ ADDRESS \_ LIST \_ SORT** ordina solo gli indirizzi IPv6. Gli indirizzi IPv4 nel formato di indirizzo IPv6 mappato a IPv4 non sono supportati.

Nell'output, il **membro iAddressCount** della struttura [**SOCKET ADDRESS \_ \_ LIST**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) può essere più piccolo rispetto all'input se il codice IOCTL determina che alcuni indirizzi di destinazione non sono validi.

## <a name="sorting-determination"></a>Determinazione dell'ordinamento

L'ordinamento per gli indirizzi IPv6 per SIO \_ ADDRESS \_ LIST SORT \_ IOCTL si basa sulla tabella dei criteri del prefisso. La tabella dei criteri  di prefisso viene configurata tramite lNetsh.exeutilizzazione della riga di comando. I frammenti di codice della riga di comando seguenti illustrano i *comandi diNetsh.exe* di configurazione della tabella dei criteri di prefisso di base:

``` syntax
netsh interface ipv6 show prefixpolicies
netsh interface ipv6 add prefixpolicy ::/96 3 4
netsh interface ipv6 delete prefixpolicy ::/96
netsh interface ipv6 set prefixpolicy ::/96 3 4
```

> [!Note]  
> In Windows Server 2003 e Windows XP, il primo comando netsh elencato in precedenza era il seguente. Tutti gli altri comandi correlati sono gli stessi.

 

``` syntax
netsh interface ipv6 show prefixpolicy
```

L'ordinamento degli indirizzi è determinato anche da un algoritmo descritto in RFC 3484 on *Default Address Selection for Internet Protocol versione 6 (IPv6)* pubblicato da IETF. Per altre informazioni, vedere [https://www.ietf.org/rfc/rfc3484.txt](https://tools.ietf.org/html/rfc3484). Questa risorsa può essere disponibile solo in inglese.

**L'IOCTL SIO \_ ADDRESS \_ LIST \_ SORT** ordina gli indirizzi dal migliore al peggiore e compila i membri ID ambito **sin6, \_ \_** se necessario. Per gli indirizzi locali del sito, SIO ADDRESS LIST SORT compila \_ \_ \_ scope-id o rimuove l'indirizzo.

**SIO \_ ADDRESS \_ LIST \_ SORT** IOCTL ignora l'indirizzo di origine associato al socket e ordina solo in base all'elenco di indirizzi di destinazione passato come parametro.

È consigliabile usare la funzione [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) invece di **SIO \_ ADDRESS LIST \_ \_ SORT** IOCTL Windows Vista e versioni successive. La **funzione CreateSortedAddressPairs** restituisce un elenco di coppie di indirizzi che contiene un indirizzo di origine locale e un indirizzo di destinazione. In questo modo un'applicazione fornisce l'indirizzo di origine corretto da usare per ogni indirizzo di destinazione. Un'applicazione può anche filtrare i risultati cercando un indirizzo di origine specifico. nei risultati.

## <a name="requirements"></a>Requisiti

**L'elemento SIO \_ ADDRESS LIST \_ \_ SORT** IOCTL è definito nel file di *intestazione Winsock2.h.* In Microsoft Windows Software Development Kit (SDK) rilasciato per Windows Vista e versioni successive, l'organizzazione dei file di intestazione è stata modificata e **SIO \_ ADDRESS LIST \_ \_ SORT** IOCTL è definito nel file di intestazione *Ws2def.h.* Si noti che il file di *intestazione Ws2def.h* viene incluso automaticamente in *Winsock2.h* e non deve mai essere usato direttamente.

**SIO \_ ADDRESS \_ LIST \_ SORT** IOCTL è supportato in Windows XP e versioni successive.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs)
</dt> </dl>

 

 
