---
title: Valori del Registro di sistema del metodo peer EAP
description: Informazioni sui valori del Registro di sistema specifici necessari per i metodi peer EAP. Visualizzare un elenco di valori del Registro di sistema e visualizzare altre risorse disponibili.
ms.assetid: 16bdd6bf-9eab-40a8-a2d3-8942d2f5f37a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2a1092b743ae0568093a563e318c3a3d24761bb634fdcfb2780c6c681fe7322
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984251"
---
# <a name="eap-peer-method-registry-values"></a>Valori del Registro di sistema del metodo peer EAP

Per i metodi peer EAP sono necessari valori specifici del Registro di sistema.

## <a name="eap-peer-method-dll-paths"></a>Percorsi DLL dei metodi peer EAP

Il percorso seguente specifica il percorso del Registro di sistema per le NORMALI DLL dei metodi peer EAP.

**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ Methods \\ *&lt; AuthorId &gt;* \\ * &lt; EapTypeId&gt;***

Ad esempio, un percorso di registrazione dell'installazione del metodo EAP dato un **AuthorId** "311" (che indica che "Microsoft" è l'autore) e un **EapTypeId** di "40", viene visualizzato come segue.

**HKLM \\ System \\ CCS Services \\ \\ Eaphost \\ Methods \\ 311 \\ 40**

Il percorso seguente specifica il percorso del Registro di sistema per le DLL estese dei metodi EAP.

> [!Note]  
> Le DLL dei metodi EAP estesi sono supportate in Windows Vista con Service Pack 1 (SP1) o versioni successive.

 

**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ Methods \\ *&lt; AuthorId &gt;* \\ 254 \\ *&lt; VendorId &gt;* \\ * &lt; EapTypeId&gt;***

Ad esempio, un percorso di registrazione di installazione del metodo EAP dato un **AuthorId** di "311" (che indica che "Microsoft" è l'autore), un **VendorId** di "311" e un **EapTypeId** di "40", viene visualizzato come segue.

**HKLM \\ System \\ CCS Services \\ \\ Eaphost \\ Methods \\ 311 \\ 254 \\ 311 \\ 40**

> [!Note]  
> Per altre informazioni sull'allocazione dei tipi di metodo EAP, vedere la sezione 6.2 di [RFC 3748.](https://go.microsoft.com/fwlink/p/?linkid=84016)

 

## <a name="registry-values"></a>Valori del Registro di sistema

I valori del Registro di sistema del metodo peer EAPHost seguenti sono obbligatori.

-   [PeerDllPath](#peerdllpath)
-   [PeerFriendlyName](#peerfriendlyname)
-   [PeerInvokePasswordDialog](#peerinvokepassworddialog)
-   [PeerInvokeUsernameDialog](#peerinvokeusernamedialog)

Sono consigliati i valori del Registro di sistema del metodo peer AP seguenti.

-   [Proprietà](#properties)

I valori del Registro di sistema del metodo peer AP seguenti sono facoltativi.

-   [PeerConfigUIPath](#peerconfiguipath)
-   [PeerIdentityPath](#peeridentitypath)
-   [PeerInteractiveUIPath](#peerinteractiveuipath)
-   [PeerRequireConfigUI](#peerrequireconfigui)

### <a name="peerconfiguipath"></a>PeerConfigUIPath



| Constant Value | PeerConfigUIPath                                                                                                                                       |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ EXPAND \_ SZ                                                                                                                                        |
| Descrizione    | Percorso della DLL che contiene l'implementazione della finestra di dialogo di configurazione utente. Ad esempio, %SystemRoot% \\ system32 \\ &lt; name of DLL \_ \_ &gt;.dll. |



 

### <a name="peerdllpath"></a>PeerDllPath



| Constant Value | PeerDllPath                                                                                     |
|----------------|-------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ EXPAND \_ SZ                                                                                 |
| Descrizione    | Percorso della DLL del metodo EAP. Ad esempio, %SystemRoot% \\ system32 \\ &lt; name of DLL \_ \_ &gt;.dll. |



 

### <a name="peerfriendlyname"></a>PeerFriendlyName



| Constant Value | PeerFriendlyName                                                     |
|----------------|----------------------------------------------------------------------|
| Tipo           | REG \_ SZ                                                              |
| Descrizione    | Stringa contenente il nome descrittivo (visualizzato) per il metodo EAP. |



 

### <a name="peeridentitypath"></a>PeerIdentityPath



| Constant Value | PeerIdentityPath                                                                                                                                     |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ EXPAND \_ SZ                                                                                                                                      |
| Descrizione    | Percorso della DLL che contiene l'implementazione delle funzioni di identità utente. Ad esempio, %SystemRoot% \\ system32 \\ &lt; name of DLL \_ \_ &gt;.dll. |



 

### <a name="peerinteractiveuipath"></a>PeerInteractiveUIPath



| Constant Value | PeerInteractiveUIPath                                                                                                                                                                                                      |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ EXPAND \_ SZ                                                                                                                                                                                                            |
| Descrizione    | Percorso della DLL che contiene l'implementazione dell'interfaccia utente interattiva utilizzata per ottenere informazioni utente durante l'esecuzione del metodo EAP. Ad esempio, %SystemRoot% \\ system32 \\ &lt; name of DLL \_ \_ &gt;.dll. |



 

### <a name="peerinvokepassworddialog"></a>PeerInvokePasswordDialog



| Constant Value | PeerInvokePasswordDialog                                                                                                                                                                                                                         |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ DWORD                                                                                                                                                                                                                                       |
| Descrizione    | 1- per ottenere le credenziali usando la finestra di dialogo generica password e dominio EAPHost. 0 : per usare una finestra di dialogo personalizzata. Se viene usata la finestra di dialogo generica, le credenziali vengono impostate dal [**metodo EapPeerSetCredentials.**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials) |



 

### <a name="peerinvokeusernamedialog"></a>PeerInvokeUsernameDialog



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Constant Value</th>
<th>PeerInvokeUsernameDialog</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tipo</td>
<td>REG_DWORD</td>
</tr>
<tr class="even">
<td>Descrizione</td>
<td><ul>
<li>1 : per ottenere le credenziali usando la finestra di dialogo generica nome utente EAPHost.</li>
<li>0- per usare una finestra di dialogo personalizzata.</li>
</ul>
Se viene usata la finestra di dialogo generica, le credenziali vengono impostate dal metodo [<strong>EapPeerSetCredentials</strong>](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials).</td>
</tr>
</tbody>
</table>



 

### <a name="peerrequireconfigui"></a>PeerRequireConfigUI



| Constant Value | PeerRequireConfigUI                                                                        |
|----------------|--------------------------------------------------------------------------------------------|
| Tipo           | REG \_ DWORD                                                                                 |
| Descrizione    | 0 se viene implementata una finestra di dialogo dell'interfaccia utente di configurazione per questo metodo. 1 in caso non lo sia. |



 

### <a name="properties"></a>Proprietà



| Constant Value | Proprietà                                                                                                                                                  |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ DWORD                                                                                                                                                  |
| Descrizione    | I bit nel valore DWORD vengono impostati per indicare il supporto per la proprietà . Per un elenco dei valori supportati, vedere [**Proprietà del metodo EAP**](eap-method-properties.md). |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Chiavi del Registro Authenticator metodo EAP](eap-authenticator-method-registry-keys.md)
</dt> <dt>

[Configurazione del Registro di sistema per i tipi EAP espansi](registry-keys-for-eap-methods.md)
</dt> <dt>

[Uso di EAPHost](using-eap-host.md)
</dt> <dt>

[RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016)
</dt> </dl>

 

 