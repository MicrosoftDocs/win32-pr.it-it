---
title: Valori del registro di sistema del metodo peer EAP
description: Informazioni sui valori specifici del registro di sistema necessari per i metodi peer EAP. Vedere un elenco di valori del registro di sistema e visualizzare altre risorse disponibili.
ms.assetid: 16bdd6bf-9eab-40a8-a2d3-8942d2f5f37a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796260a25f824ffe52ada7cdfadfb7a25f05d491
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339286"
---
# <a name="eap-peer-method-registry-values"></a>Valori del registro di sistema del metodo peer EAP

Per i metodi peer EAP sono necessari valori specifici del registro di sistema.

## <a name="eap-peer-method-dll-paths"></a>Percorsi DLL del metodo peer EAP

Il percorso seguente specifica il percorso del registro di sistema per le DLL regolari del metodo peer EAP.

**HKLM \\ System \\ CCS \\ Services \\ EAPHost \\ metodi \\ *&lt; autorizzati &gt;* \\ * &lt; EapTypeId&gt;***

Un percorso di registrazione per l'installazione di un metodo EAP, ad esempio, dato un **autorizzazione** di "311" (che indica che "Microsoft" è l'autore) e un **EapTypeId** di "40", viene visualizzato come segue.

**HKLM \\ System \\ CCS \\ Services \\ ( \\ metodi EAPHost) \\ 311 \\ 40**

Il percorso seguente specifica il percorso del registro di sistema per le dll del metodo EAP estese.

> [!Note]  
> Le DLL dei metodi EAP estesi sono supportate in Windows Vista con Service Pack 1 (SP1) o versioni successive.

 

**HKLM \\ System \\ CCS \\ Services \\ EAPHost \\ Methods \\ *&lt; autorizzato &gt;* \\ 254 \\ *&lt; VendorID &gt;* \\ * &lt; EapTypeId&gt;***

Un percorso di registrazione per l'installazione di un metodo EAP, ad esempio, dato un oggetto **autorizzato** di "311" (che indica che "Microsoft" è l'autore), un **VendorId** di "311" e un **EapTypeId** di "40" viene visualizzato come segue.

**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ methods \\ 311 \\ 254 \\ 311 \\ 40**

> [!Note]  
> Per ulteriori informazioni sull'allocazione dei tipi di metodo EAP, vedere la sezione 6,2 della [specifica RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).

 

## <a name="registry-values"></a>Valori del registro di sistema

Sono necessari i seguenti valori del registro di sistema del peer EAPHost.

-   [PeerDllPath](#peerdllpath)
-   [PeerFriendlyName](#peerfriendlyname)
-   [PeerInvokePasswordDialog](#peerinvokepassworddialog)
-   [PeerInvokeUsernameDialog](#peerinvokeusernamedialog)

Sono consigliati i seguenti valori del registro di sistema del peer di AP.

-   [Proprietà](#properties)

I valori del registro di sistema del peer AP seguenti sono facoltativi.

-   [PeerConfigUIPath](#peerconfiguipath)
-   [PeerIdentityPath](#peeridentitypath)
-   [PeerInteractiveUIPath](#peerinteractiveuipath)
-   [PeerRequireConfigUI](#peerrequireconfigui)

### <a name="peerconfiguipath"></a>PeerConfigUIPath



| Constant Value | PeerConfigUIPath                                                                                                                                       |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ Espandi \_ SZ                                                                                                                                        |
| Descrizione    | Percorso della DLL che contiene l'implementazione della finestra di dialogo di configurazione dell'utente. Ad esempio,% SystemRoot% \\ system32 \\ &lt; nome \_ di \_ dll &gt; . dll. |



 

### <a name="peerdllpath"></a>PeerDllPath



| Constant Value | PeerDllPath                                                                                     |
|----------------|-------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ Espandi \_ SZ                                                                                 |
| Descrizione    | Percorso della DLL del metodo EAP. Ad esempio,% SystemRoot% \\ system32 \\ &lt; nome \_ di \_ dll &gt; . dll. |



 

### <a name="peerfriendlyname"></a>PeerFriendlyName



| Constant Value | PeerFriendlyName                                                     |
|----------------|----------------------------------------------------------------------|
| Tipo           | REG \_ SZ                                                              |
| Descrizione    | Stringa che contiene il nome descrittivo (visualizzazione) per il metodo EAP. |



 

### <a name="peeridentitypath"></a>PeerIdentityPath



| Constant Value | PeerIdentityPath                                                                                                                                     |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ Espandi \_ SZ                                                                                                                                      |
| Descrizione    | Percorso della DLL che contiene l'implementazione delle funzioni di identità utente. Ad esempio,% SystemRoot% \\ system32 \\ &lt; nome \_ di \_ dll &gt; . dll. |



 

### <a name="peerinteractiveuipath"></a>PeerInteractiveUIPath



| Constant Value | PeerInteractiveUIPath                                                                                                                                                                                                      |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ Espandi \_ SZ                                                                                                                                                                                                            |
| Descrizione    | Percorso della DLL che contiene l'implementazione dell'interfaccia utente interattiva utilizzata per ottenere informazioni sull'utente durante l'esecuzione del metodo EAP. Ad esempio,% SystemRoot% \\ system32 \\ &lt; nome \_ di \_ dll &gt; . dll. |



 

### <a name="peerinvokepassworddialog"></a>PeerInvokePasswordDialog



| Constant Value | PeerInvokePasswordDialog                                                                                                                                                                                                                         |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ DWORD                                                                                                                                                                                                                                       |
| Descrizione    | 1-per ottenere le credenziali tramite la finestra di dialogo Generic EAPHost password and Domain. 0: per utilizzare una finestra di dialogo personalizzata. Se viene utilizzata la finestra di dialogo generica, le credenziali vengono impostate dal metodo [**EapPeerSetCredentials**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials) . |



 

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
<li>1-per ottenere le credenziali utilizzando la finestra di dialogo nome utente generico EAPHost.</li>
<li>0: per utilizzare una finestra di dialogo personalizzata.</li>
</ul>
Se viene utilizzata la finestra di dialogo generica, le credenziali vengono impostate dal metodo [<strong>EapPeerSetCredentials</strong>] (/Previous-Versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeersetcredentials).</td>
</tr>
</tbody>
</table>



 

### <a name="peerrequireconfigui"></a>PeerRequireConfigUI



| Constant Value | PeerRequireConfigUI                                                                        |
|----------------|--------------------------------------------------------------------------------------------|
| Tipo           | REG \_ DWORD                                                                                 |
| Descrizione    | 0 se viene implementata una finestra di dialogo dell'interfaccia utente di configurazione per questo metodo; 1 in caso contrario. |



 

### <a name="properties"></a>Proprietà



| Constant Value | Proprietà                                                                                                                                                  |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ DWORD                                                                                                                                                  |
| Descrizione    | I bit in DWORD sono impostati per indicare il supporto per la proprietà. Per un elenco dei valori supportati, vedere [**proprietà del metodo EAP**](eap-method-properties.md). |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Chiavi del registro di sistema EAP Authenticator](eap-authenticator-method-registry-keys.md)
</dt> <dt>

[Configurazione del registro di sistema per i tipi EAP espansi](registry-keys-for-eap-methods.md)
</dt> <dt>

[Uso di EAPHost](using-eap-host.md)
</dt> <dt>

[RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016)
</dt> </dl>

 

 