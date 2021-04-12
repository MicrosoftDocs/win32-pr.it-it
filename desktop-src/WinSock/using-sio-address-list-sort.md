---
description: L' \_ ordinamento dell' \_ elenco di indirizzi sio \_ consente agli sviluppatori di applicazioni di ordinare un elenco di indirizzi IPv6 e IPv4 di destinazione per determinare il migliore indirizzo disponibile per l'esecuzione di una connessione. L' \_ ordinamento dell'elenco di indirizzi sio \_ \_ è supportato in Windows XP e versioni successive.
ms.assetid: bf380ddf-8171-4ef4-be47-94c7a6aabf0a
title: Utilizzo di SIO_ADDRESS_LIST_SORT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6452023b69ccf72c78b393c5059fee497997af51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233483"
---
# <a name="using-sio_address_list_sort"></a>Uso dell' \_ \_ ordinamento dell'elenco di indirizzi sio \_

L' **\_ ordinamento dell' \_ elenco \_ di indirizzi sio** consente agli sviluppatori di applicazioni di ordinare un elenco di indirizzi IPv6 e IPv4 di destinazione per determinare il migliore indirizzo disponibile per l'esecuzione di una connessione. L' **\_ ordinamento dell' \_ elenco \_ di indirizzi sio** è supportato in Windows XP e versioni successive.

In Windows Vista e versioni successive, la funzione [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) accetta un elenco fornito di indirizzi IP di destinazione potenziali, associa gli indirizzi di destinazione agli indirizzi IP locali del computer host e ordina le coppie in base alla coppia di indirizzi più adatta per la comunicazione tra i due peer. La funzione **CreateSortedAddressPairs** deve essere utilizzata al posto dell' **elenco di indirizzi Sio di \_ \_ \_ ordinamento** in Windows Vista e versioni successive.

Le sezioni seguenti descrivono le considerazioni sull'utilizzo per l' **\_ ordinamento dell' \_ elenco \_ di indirizzi sio**.

## <a name="parameters"></a>Parametri

Il buffer passato all' **\_ ordinamento dell' \_ elenco \_ di indirizzi sio** è una struttura dell' [**\_ \_ elenco di indirizzi del socket**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) . Ogni [**\_ indirizzo del socket**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) nell'elenco deve essere in \_ formato sockaddr IN6.

L' **\_ ordinamento dell' \_ elenco \_ di indirizzi sio** Ordina gli indirizzi IPv6 e IPv4 in Windows Vista e versioni successive. Tutti gli indirizzi IPv4 nell'elenco da ordinare devono essere nel formato di indirizzo IPv6 mappato a IPv4. Per ulteriori informazioni sul formato degli indirizzi IPv6 con mapping IPv4, vedere [socket a doppio stack](dual-stack-sockets.md).

In Windows Server 2003 e Windows XP, l' **\_ ordinamento dell' \_ elenco \_ di indirizzi sio** Ordina solo gli indirizzi IPv6. Gli indirizzi IPv4 nel formato di indirizzo IPv6 con mapping IPv4 non sono supportati.

Nell'output, il membro **iAddressCount** della struttura [**dell' \_ \_ elenco di indirizzi del socket**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) può essere minore dell'input se il codice IOCTL determina che alcuni indirizzi di destinazione non sono validi.

## <a name="sorting-determination"></a>Determinazione dell'ordinamento

L'ordinamento degli indirizzi IPv6 per l' \_ ordinamento dell'elenco di indirizzi sio \_ \_ è basato sulla tabella dei criteri di prefisso. La tabella dei criteri di prefisso viene configurata tramite l'utilità da riga di comando *Netsh.exe* . I frammenti di codice seguenti della riga di comando illustrano i comandi di configurazione della tabella dei criteri di base *Netsh.exe* prefisso:

``` syntax
netsh interface ipv6 show prefixpolicies
netsh interface ipv6 add prefixpolicy ::/96 3 4
netsh interface ipv6 delete prefixpolicy ::/96
netsh interface ipv6 set prefixpolicy ::/96 3 4
```

> [!Note]  
> In Windows Server 2003 e Windows XP il primo comando netsh elencato sopra è il seguente. Tutti gli altri comandi correlati sono uguali.

 

``` syntax
netsh interface ipv6 show prefixpolicy
```

L'ordinamento degli indirizzi è determinato anche da un algoritmo descritto nella specifica RFC 3484 sulla *selezione di indirizzi predefiniti per il protocollo IP versione 6 (IPv6)* pubblicata da IETF. Per altre informazioni, vedere [https://www.ietf.org/rfc/rfc3484.txt](https://tools.ietf.org/html/rfc3484). Questa risorsa può essere disponibile solo in inglese.

L' **\_ ordinamento dell' \_ elenco \_ di indirizzi sio** Ordina gli indirizzi dal migliore al peggiore e compila i membri con **\_ \_ ID ambito sin6** , se necessario. Per gli indirizzi locali del sito, l' \_ ordinamento dell'elenco di indirizzi sio \_ \_ riempie l'ID ambito o rimuove l'indirizzo.

L' **\_ ordinamento dell' \_ elenco \_ di indirizzi sio** ignora l'indirizzo di origine associato al socket e ordina in base all'elenco di indirizzi di destinazione passato come parametro.

La funzione [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) deve essere utilizzata al posto dell' **elenco di indirizzi Sio di \_ \_ \_ ordinamento** in Windows Vista e versioni successive. La funzione **CreateSortedAddressPairs** restituisce un elenco di coppie di indirizzi che contengono un indirizzo di origine locale e un indirizzo di destinazione. Fornisce a un'applicazione l'indirizzo di origine corretto da usare per ogni indirizzo di destinazione. Un'applicazione può anche filtrare i risultati cercando un indirizzo di origine specifico. nei risultati.

## <a name="requirements"></a>Requisiti

L' **\_ ordinamento dell' \_ elenco \_ di indirizzi sio** è definito nel file di intestazione *Winsock2. h* . In Microsoft Windows Software Development Kit (SDK) rilasciata per Windows Vista e versioni successive, l'organizzazione dei file di intestazione è stata modificata e l' **\_ ordinamento dell' \_ elenco \_ di indirizzi sio** è definito nel file di intestazione *Ws2def. h* . Si noti che il file di intestazione *Ws2def. h* viene incluso automaticamente in *Winsock2. h* e non deve mai essere utilizzato direttamente.

L' **\_ ordinamento dell' \_ elenco \_ di indirizzi sio** è supportato in Windows XP e versioni successive.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs)
</dt> </dl>

 

 
