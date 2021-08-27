---
title: Proprietà del metodo EAP (Eaptypes.h)
description: Usato da supplicant e autenticatori per determinare i metodi EAP da usare con un determinato supplicante o autenticatore. Le proprietà del metodo specificano anche la configurazione di un metodo.
ms.assetid: 10407b85-5d2c-4c75-9b65-a0d65d4cc7ab
topic_type:
- apiref
api_name:
- eapPropCipherSuiteNegotiation
- eapPropMutualAuth
- eapPropIntegrity
- eapPropReplayProtection
- eapPropConfidentiality
- eapPropKeyDerivation
- eapPropKeyStrength64
- eapPropKeyStrength128
- eapPropKeyStrength256
- eapPropKeyStrength512
- eapPropKeyStrength1024
- eapPropDictionaryAttackResistance
- eapPropFastReconnect
- eapPropCryptoBinding
- eapPropSessionIndependence
- eapPropFragmentation
- eapPropChannelBinding
- eapPropNap
- eapPropStandalone
- eapPropMppeEncryption
- eapPropTunnelMethod
- eapPropSupportsConfig
- eapPropCertifiedMethod
- eapPropmachineAuth
- eapPropUserAuth
- eapPropIdentityPrivacy
- eapPropMethodChaining
- eapPropSharedStateEquivalence
- eapPropReserved
api_location:
- eaptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c88c31d77b666e377cbd1911cde8b5df63d8f5c2fc750cd03a701b03af5b60ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094401"
---
# <a name="eap-method-properties"></a>Proprietà del metodo EAP

Usato da supplicant e autenticatori per determinare i metodi EAP da usare con un determinato supplicante o autenticatore. Le proprietà del metodo specificano anche la configurazione di un metodo.

Ad esempio, il supplicante [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) può richiedere che i metodi abbia determinate proprietà da usare con il supplicant [802.1X.](/previous-versions/windows/embedded/ms890287(v=msdn.10)) Il materiale per la chiave, ad esempio, è un requisito.

Sono elencate le proprietà supportate dai metodi EAP. Le proprietà vengono archiviate come valori delle chiavi del Registro di sistema. Per altre informazioni, vedere la sezione EAP Peer Method DLL Registry Key dell'argomento [Registry Configuration for EAP Methods.](registry-keys-for-eap-methods.md)

<dl> <dt>

<span id="eapPropCipherSuiteNegotiation"></span><span id="eappropciphersuitenegotiation"></span><span id="EAPPROPCIPHERSUITENEGOTIATION"></span>**eapPropCipherSuiteNegotiation**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Il metodo consente la negoziazione del pacchetto di crittografia ai fini della crittografia dei dati. Windows Server 2008 supporta i pacchetti di crittografia 3DES [seguenti:](/windows/desktop/SecAuthN/tls-cipher-suites)

-   TLS \_ RSA \_ CON \_ 3DES \_ EDE \_ CBC SHA \_ (TLS & SSL 3)
-   TLS \_ DHE \_ DSS \_ CON \_ 3DES \_ EDE \_ CBC SHA \_ (TLS & SSL 3)
-   SSL \_ CK \_ DES \_ 192 \_ EDE3 \_ CBC WITH \_ \_ MD5 (SSL 2 se abilitato)

Per altre informazioni sul protocollo di sicurezza TLS 1.0, vedere [RFC 2246.](https://go.microsoft.com/fwlink/p/?linkid=84035)


</dt> </dl> </dd> <dt>

<span id="eapPropMutualAuth"></span><span id="eappropmutualauth"></span><span id="EAPPROPMUTUALAUTH"></span>**eapPropMutualAuth**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Il metodo fornisce uno scambio in cui l'autenticatore autentica il peer e viceversa.


</dt> </dl> </dd> <dt>

<span id="eapPropIntegrity"></span><span id="eappropintegrity"></span><span id="EAPPROPINTEGRITY"></span>**eapPropIntegrity**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Il metodo fornisce l'autenticazione dell'origine dati e la protezione da modifiche non autorizzate delle informazioni per i pacchetti EAP, incluse le richieste e le risposte EAP. Quando si effettua questa attestazione, una specifica del metodo deve specificare i pacchetti EAP protetti e i campi protetti all'interno dei pacchetti EAP.


</dt> </dl> </dd> <dt>

<span id="eapPropReplayProtection"></span><span id="eappropreplayprotection"></span><span id="EAPPROPREPLAYPROTECTION"></span>**eapPropReplayProtection**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Il metodo può proteggersi dalla riproduzione di un metodo EAP o dei relativi messaggi. Le indicazioni di esito positivo e negativo non possono essere riprodotte.


</dt> </dl> </dd> <dt>

<span id="eapPropConfidentiality"></span><span id="eappropconfidentiality"></span><span id="EAPPROPCONFIDENTIALITY"></span>**eapPropConfidentiality**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Il metodo può crittografare i messaggi EAP. Le richieste EAP, le risposte EAP, le indicazioni dei risultati di esito positivo e le indicazioni dei risultati degli errori vengono crittografate. Un metodo che effettua questa attestazione deve supportare identity protection.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyDerivation"></span><span id="eappropkeyderivation"></span><span id="EAPPROPKEYDERIVATION"></span>**eapPropKeyDerivation**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Il metodo può derivare materiale esportabile per la chiave, ad esempio la chiave della sessione master (MSK) e la chiave della sessione master estesa (EMSK). La chiave MSK viene usata solo per un'ulteriore derivazione della chiave, non direttamente per la protezione della conversazione EAP o dei dati successivi. L'uso di EMSK è riservato.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength64"></span><span id="eappropkeystrength64"></span><span id="EAPPROPKEYSTRENGTH64"></span>**eapPropKeyStrength64**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



La lunghezza minima della chiave supportata dal metodo EAP è 64 bit.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength128"></span><span id="eappropkeystrength128"></span><span id="EAPPROPKEYSTRENGTH128"></span>**eapPropKeyStrength128**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



La lunghezza minima della chiave supportata dal metodo EAP è 128 bit.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength256"></span><span id="eappropkeystrength256"></span><span id="EAPPROPKEYSTRENGTH256"></span>**eapPropKeyStrength256**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



La lunghezza minima della chiave supportata dal metodo EAP è 256 bit.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength512"></span><span id="eappropkeystrength512"></span><span id="EAPPROPKEYSTRENGTH512"></span>**eapPropKeyStrength512**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



La lunghezza minima della chiave supportata dal metodo EAP è 512 bit.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength1024"></span><span id="eappropkeystrength1024"></span><span id="EAPPROPKEYSTRENGTH1024"></span>**eapPropKeyStrength1024**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



La lunghezza minima della chiave supportata dal metodo EAP è 1024 bit.


</dt> </dl> </dd> <dt>

<span id="eapPropDictionaryAttackResistance"></span><span id="eappropdictionaryattackresistance"></span><span id="EAPPROPDICTIONARYATTACKRESISTANCE"></span>**eapPropDictionaryAttackResistance**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



Il metodo non consente un attacco offline con un fattore di lavoro basato sul numero di password nel dizionario di un utente malintenzionato. Quando viene usata l'autenticazione della password, le password vengono in genere selezionate da un set di piccole dimensioni (rispetto a un set di chiavi a N bit), che genera un problema per gli attacchi al dizionario. Si può dire che un metodo fornisce protezione dagli attacchi con dizionario se, quando usa una password come segreto, il metodo non consente un attacco offline con un fattore di lavoro basato sul numero di password nel dizionario di un utente malintenzionato.


</dt> </dl> </dd> <dt>

<span id="eapPropFastReconnect"></span><span id="eappropfastreconnect"></span><span id="EAPPROPFASTRECONNECT"></span>**eapPropFastReconnect**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



Il metodo ha la possibilità, nel caso in cui sia stata precedentemente stabilita un'associazione di sicurezza, di creare un'associazione di sicurezza nuova o aggiornata in modo più efficiente o in un numero minore di round trip.


</dt> </dl> </dd> <dt>

<span id="eapPropCryptoBinding"></span><span id="eappropcryptobinding"></span><span id="EAPPROPCRYPTOBINDING"></span>**eapPropCryptoBinding**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Il metodo dimostra al server EAP che una singola entità ha fungeto da peer EAP per tutti i metodi eseguiti all'interno di un metodo di tunnel. L'associazione può anche implicare che il server EAP dimostra al peer che una singola entità ha fungeto da server EAP per tutti i metodi eseguiti all'interno di un metodo di tunnel. Se eseguito correttamente, il binding serve a mitigare le vulnerabilità man-in-the-middle.


</dt> </dl> </dd> <dt>

<span id="eapPropSessionIndependence"></span><span id="eappropsessionindependence"></span><span id="EAPPROPSESSIONINDEPENDENCE"></span>**eapPropSessionIndependence**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



Il metodo dimostra che gli attacchi passivi (ad esempio l'acquisizione della conversazione EAP) o gli attacchi attivi (inclusa la compromissione di MSK o EMSK) non compromette gli MSK o gli EMSK successivi o precedenti.


</dt> </dl> </dd> <dt>

<span id="eapPropFragmentation"></span><span id="eappropfragmentation"></span><span id="EAPPROPFRAGMENTATION"></span>**eapPropFragmentation**
</dt> <dd> <dl> <dt>

0x00008000
</dt> <dt>



Il metodo può supportare la frammentazione e il riassemblaggio se i pacchetti EAP superano il valore minimo di MTU (unità massima di trasmissione) di 1020 ottetti.


</dt> </dl> </dd> <dt>

<span id="eapPropChannelBinding"></span><span id="eappropchannelbinding"></span><span id="EAPPROPCHANNELBINDING"></span>**eapPropChannelBinding**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



Il metodo può comunicare le proprietà del canale protetto dall'integrità, ad esempio gli identificatori di endpoint, che possono essere confrontati con i valori comunicati tramite meccanismi fuori banda, ad esempio un protocollo di [autenticazione,](https://go.microsoft.com/fwlink/p/?linkid=84063) autorizzazione e accounting (AAA) o il protocollo di livello inferiore.


</dt> </dl> </dd> <dt>

<span id="eapPropNap"></span><span id="eappropnap"></span><span id="EAPPROPNAP"></span>**eapPropNap**
</dt> <dd> <dl> <dt>

 0x00020000
</dt> <dt>



Il metodo supporta Protezione accesso alla rete.


</dt> </dl> </dd> <dt>

<span id="eapPropStandalone"></span><span id="eappropstandalone"></span><span id="EAPPROPSTANDALONE"></span>**eapPropStandalone**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



Il metodo può essere usato in un computer autonomo.


</dt> </dl> </dd> <dt>

<span id="eapPropMppeEncryption"></span><span id="eappropmppeencryption"></span><span id="EAPPROPMPPEENCRYPTION"></span>**eapPropMppeEncryption**
</dt> <dd> <dl> <dt>

 0x00080000
</dt> <dt>



Il metodo supporta la crittografia del protocollo [MPPE (Microsoft Point-to-Point](https://go.microsoft.com/fwlink/p/?linkid=83915) Encryption).


</dt> </dl> </dd> <dt>

<span id="eapPropTunnelMethod"></span><span id="eapproptunnelmethod"></span><span id="EAPPROPTUNNELMETHOD"></span>**eapPropTunnelMethod**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



Il metodo supporta il tunneling di altri metodi EAP.


</dt> </dl> </dd> <dt>

<span id="eapPropSupportsConfig"></span><span id="eappropsupportsconfig"></span><span id="EAPPROPSUPPORTSCONFIG"></span>**eapPropSupportsConfig**
</dt> <dd> <dl> <dt>

0x00200000
</dt> <dt>



Il metodo supporta le proprietà configurabili e dispone di un'interfaccia utente.


</dt> </dl> </dd> <dt>

<span id="eapPropCertifiedMethod"></span><span id="eappropcertifiedmethod"></span><span id="EAPPROPCERTIFIEDMETHOD"></span>**eapPropCertifiedMethod**
</dt> <dd> <dl> <dt>

0x00400000
</dt> <dt>



Il metodo è stato certificato dal programma di certificazione EAP. Questo bit deve essere inviato solo dai metodi EAP che hanno superato la certificazione.


</dt> </dl> </dd> <dt>

<span id="eapPropmachineAuth"></span><span id="eappropmachineauth"></span><span id="EAPPROPMACHINEAUTH"></span>**eapPropmachineAuth**
</dt> <dd> <dl> <dt>

0x01000000
</dt> <dt>



Windows 7 o versione successiva: il metodo può essere usato per autenticare un computer in una rete usando le credenziali del computer.


</dt> </dl> </dd> <dt>

<span id="eapPropUserAuth"></span><span id="eappropuserauth"></span><span id="EAPPROPUSERAUTH"></span>**eapPropUserAuth**
</dt> <dd> <dl> <dt>

0x02000000
</dt> <dt>



Windows 7 o versione successiva: il metodo può essere usato per autenticare un utente in una rete usando le credenziali dell'utente.


</dt> </dl> </dd> <dt>

<span id="eapPropIdentityPrivacy"></span><span id="eappropidentityprivacy"></span><span id="EAPPROPIDENTITYPRIVACY"></span>**eapPropIdentityPrivacy**
</dt> <dd> <dl> <dt>

0x04000000
</dt> <dt>



Windows 7 o versione successiva: il metodo supporta l'invio dell'identità utente in un canale protetto.


</dt> </dl> </dd> <dt>

<span id="eapPropMethodChaining"></span><span id="eappropmethodchaining"></span><span id="EAPPROPMETHODCHAINING"></span>**eapPropMethodChaining**
</dt> <dd> <dl> <dt>

0x08000000
</dt> <dt>



Windows 7 o versione successiva: il metodo è un metodo con tunneling e supporta il concatenamento dei metodi EAP all'interno del tunnel.


</dt> </dl> </dd> <dt>

<span id="eapPropSharedStateEquivalence"></span><span id="eappropsharedstateequivalence"></span><span id="EAPPROPSHAREDSTATEEQUIVALENCE"></span>**eapPropSharedStateEquivalence**
</dt> <dd> <dl> <dt>

0x10000000
</dt> <dt>



Windows 7 o versione successiva: il metodo supporta l'equivalenza dello stato condiviso come definito in [RFC 4017.](https://go.microsoft.com/fwlink/p/?linkid=90455)


</dt> </dl> </dd> <dt>

<span id="eapPropReserved"></span><span id="eappropreserved"></span><span id="EAPPROPRESERVED"></span>**eapPropReserved**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>



Riservato. Non usato.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Eaptypes.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Chiavi del Registro di sistema per i metodi EAP](registry-keys-for-eap-methods.md)
</dt> <dt>

[Costanti EAPHost comuni](common-eap-host-error-constants.md)
</dt> </dl>

