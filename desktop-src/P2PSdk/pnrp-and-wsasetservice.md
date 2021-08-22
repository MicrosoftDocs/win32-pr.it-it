---
description: PNRP usa la funzione WSASetService per registrare o rimuovere i nomi peer.
ms.assetid: ea7941cd-2b3c-42d1-a291-759cbc32db0c
title: PNRP e WSASetService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afbc11e65c9d583f91b5070e960435612ad05717b6ccfe087924da133c531b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518101"
---
# <a name="pnrp-and-wsasetservice"></a>PNRP e WSASetService

PNRP usa la [**funzione WSASetService**](winsock-nsp-reference-links.md) per registrare o rimuovere i [nomi peer.](peer-names.md)

## <a name="registering-a-name"></a>Registrazione di un nome

La registrazione include un nome peer e un set di endpoint in cui è possibile contattare un servizio. Una registrazione è specifica di un cloud PNRP. Dopo la registrazione di un peer, si verifica un ritardo tra la registrazione e la propagazione delle informazioni di registrazione ad altri nodi. Durante questo periodo, altri nodi potrebbero non essere in grado di risolvere un peer appena registrato.

La registrazione del servizio non è persistente.

-   Se un processo client che registra un nome peer viene chiuso o chiama [**WSACleanup,**](winsock-nsp-reference-links.md)viene annullata la registrazione del nome peer.
-   Se un nome peer specificato è già registrato nello stesso cloud dal processo corrente, viene sostituito con nuovi valori di registrazione.

Quando si registra un nome peer, è necessario indicare i valori dei parametri seguenti:

-   *Il parametro essOperation* deve avere il valore **RNRSERVICE \_ REGISTER**.
-   *Il parametro dwControlFlags* deve essere zero (0).

Quando si registra un nome peer, la struttura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) a cui fa riferimento il *parametro lpqsRegInfo* deve contenere i valori seguenti:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Specifica le dimensioni di questa struttura.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

Specifica un nome peer da registrare. Se il [nome peer](peer-names.md) non è protetto, l'identità è facoltativa. Se l'identità viene specificata come **NULL,** PNRP usa l'identità locale del computer, per impostazione predefinita.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Deve essere SVCID \_ PNRPNAME.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Ignorato. Impostare su **NULL.**

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Ignorato. È tuttavia necessario che la stringa sia inferiore a 40 caratteri, incluso il carattere **di terminazione NULL.**

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**
</dt> <dd>

Deve essere **NS \_ PNRPNAME** o **NS \_ ALL.**

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**
</dt> <dd>

Deve essere **NS \_ PROVIDER \_ PNRPNAME** o **NULL.**

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**
</dt> <dd>

Deve essere un nome cloud, una stringa vuota o **NULL.** Se questo valore è **NULL** o una stringa vuota, viene usato il cloud predefinito"Global". In caso contrario, deve puntare a un nome di cloud valido.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

Ignorato. Impostare su zero (0).

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

Ignorato. Impostare su **NULL.**

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

Specifica il numero di indirizzi registrati da un servizio. Il numero massimo di indirizzi che è possibile registrare per un singolo nome è 10.

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

Puntatore a un elenco di indirizzi da registrare.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

Ignorato. Impostare su zero (0).

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

Puntatore a [**una struttura BLOB**](winsock-nsp-reference-links.md) che punta a una struttura [**PNRPINFO.**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) È necessario impostare parametri specifici nella struttura **PNRPINFO.** Per altre informazioni, vedere la sezione seguente **della struttura PNRPINFO.**

</dd> </dl>

## <a name="pnrpinfo-structure"></a>Struttura PNRPINFO

Se il **membro lpBlob** della struttura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) è impostato, è necessario impostare i membri seguenti della struttura [**PNRPINFO:**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Specifica le dimensioni di questa struttura.

</dd> <dt>

<span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**
</dt> <dd>

Specifica l'identità del nome peer creato tramite [**PeerIdentityCreate.**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate) Se un nome peer non è protetto, l'identità è facoltativa. Se l'identità viene specificata come **NULL,** PNRP usa l'identità locale del computer, per impostazione predefinita.

</dd> <dt>

<span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**
</dt> <dd>

Ignorato. Impostare su zero (0).

</dd> <dt>

<span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**
</dt> <dd>

Ignorato. Impostare su zero (0).

</dd> <dt>

<span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**
</dt> <dd>

Specifica il numero di secondi tra le operazioni di aggiornamento.

</dd> <dt>

<span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**
</dt> <dd>

Ignorato. Impostare su zero (0).

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**Dwflags**
</dt> <dd>

Deve essere zero (0) o **PNRPINFO \_ HINT**. Il valore predefinito è zero (0). Ciò significa che la parte relativa alla posizione del servizio dell'ID PNRP viene compilata usando l'indirizzo IP in **saHint**. In caso contrario, il percorso del servizio viene compilato usando il primo indirizzo IP nella prima voce IPv6 del **membro lpcsaBuffer.**

</dd> <dt>

<span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**saHint**
</dt> <dd>

Specifica l'indirizzo IPv6 per l'hint.

</dd> <dt>

<span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**enNameState**
</dt> <dd>

Ignorato. Impostare su zero (0).

</dd> </dl>

## <a name="unregistering-a-peer-name"></a>Annullamento della registrazione di un nome peer

L'elenco seguente identifica le informazioni importanti sull'annullamento della registrazione di un nome peer.

-   Solo un'applicazione che registra un nome peer può annullarla.
-   Un nome peer viene annullato automaticamente se [**viene chiamato WSACleanup.**](winsock-nsp-reference-links.md)
-   PNRP rimuove sempre l'intera registrazione del nome del servizio. Non consente la rimozione di singoli indirizzi.
-   Quando si annulla la registrazione di un nome, il *parametro essOperation* deve avere il valore **RNRSERVICE \_ DELETE**.
-   PNRP non supporta il valore **RNRSERVICE \_ DEREGISTER**.
-   Il *parametro dwControlFlags* deve essere zero (0).

Quando si annulla la registrazione di un nome, la struttura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) a cui fa riferimento il parametro *lpqsRegInfo* deve contenere i valori seguenti:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Specifica le dimensioni di questa struttura.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

Specifica un nome peer di cui annullare la registrazione.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Deve essere **SVCID \_ PNRPNAME**.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Ignorato. Impostare su **NULL.**

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Ignorato. Impostare su **NULL.**

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**
</dt> <dd>

Deve essere **NS \_ PNRPNAME** o **NS \_ ALL.**

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**
</dt> <dd>

Deve essere **NS \_ PROVIDER \_ PNRPNAME** o **NULL.**

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**
</dt> <dd>

Deve essere un nome cloud, una stringa vuota o **NULL.** Se questo valore è **NULL** o una stringa vuota, viene usato il cloud predefinito "Global". In caso contrario, deve puntare a un nome di cloud valido.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

Ignorato. Impostare su zero (0).

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

Ignorato. Impostare su **NULL.**

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

Ignorato. Impostare su **NULL.**

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

Ignorato. Impostare su **NULL.**

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

Ignorato. Impostare su zero (0).

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

Puntatore a [**una struttura BLOB**](winsock-nsp-reference-links.md) che punta a una struttura [**PNRPINFO.**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) Il **membro lpszIdentity** della struttura **lpBlob** identifica il nome dell'identità usata per registrare un nome peer. I membri rimanenti devono essere impostati sullo stesso valore utilizzato durante la registrazione di un nome.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[PNRP e BLOB](pnrp-and-blob.md)
</dt> <dt>

[PNRP e WSAQUERYSET](pnrp-and-wsaqueryset.md)
</dt> <dt>

[**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[Codici di errore PNRP NSP](pnrp-nsp-error-codes.md)
</dt> <dt>

[**WSACleanup**](winsock-nsp-reference-links.md)
</dt> <dt>

**WSASetService**
</dt> </dl>

 

 



