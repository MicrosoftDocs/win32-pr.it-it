---
title: Valori del registro di sistema del metodo di autenticazione EAP
description: Informazioni sui valori del registro di sistema del metodo EAP Authenticator. Questi valori specifici del registro di sistema sono necessari per i metodi di autenticazione EAP.
ms.assetid: 9374f9f7-b088-4e3a-ac96-8ccbeda87bb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a710ca6f09914c8d111c42a8323a9c39c51f898
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963469"
---
# <a name="eap-authenticator-method-registry-values"></a>Valori del registro di sistema del metodo di autenticazione EAP

Per i metodi di autenticazione EAP sono necessari valori specifici del registro di sistema.

## <a name="eap-authenticator-method-dll-paths"></a>Percorsi DLL del metodo di autenticazione EAP

Il percorso seguente specifica il percorso del registro di sistema per le dll normali del metodo di autenticazione EAP.

**HKLM \\ System \\ CCS \\ Services \\ EAPHost \\ metodi \\ *&lt; autorizzati &gt;* \\ * &lt; EapTypeId&gt;***

Ad esempio, un percorso di registrazione per l'installazione di un metodo di autenticazione EAP, dato un **autorizzazione** di "311" (che indica che "Microsoft" è l'autore) e un **EapTypeId** di "40", viene visualizzato come segue.

**HKLM \\ System \\ CCS \\ Services \\ ( \\ metodi EAPHost) \\ 311 \\ 40**

Il percorso seguente specifica il percorso del registro di sistema per le DLL dei metodi di autenticazione EAP estese.

**HKLM \\ System \\ CCS \\ Services \\ EAPHost \\ Methods \\ *&lt; autorizzato &gt;* \\ 254 \\ *&lt; VendorID &gt;* \\ * &lt; VendorType&gt;***

Ad esempio, un percorso di registrazione per l'installazione di un metodo di autenticazione EAP, dato un **autorizzazione** di "311" (che indica che "Microsoft" è l'autore), un **VendorId** di "311" e un **EapTypeId** di "40", viene visualizzato come segue.

**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ methods \\ 311 \\ 254 \\ 311 \\ 40**

> [!Note]  
> Per ulteriori informazioni sull'allocazione dei tipi di metodo EAP, vedere la sezione 6,2 della [specifica RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).

 

## <a name="registry-values"></a>Valori del registro di sistema

Sono necessari i seguenti valori del registro di sistema del metodo Authenticator.

-   [AuthenticatorDllPath](#authenticatordllpath)
-   [AuthenticatorFriendlyName](#authenticatorfriendlyname)

Oltre ai valori del registro di sistema indicati di seguito, è consigliato il seguente valore del registro di sistema del metodo Authenticator.

-   [Proprietà](#properties)

I valori del registro di sistema del metodo Authenticator rimanenti sono facoltativi.

-   [ConfigCLSID](#configclsid)
-   [StandaloneSupported](#standalonesupported)

## <a name="authenticatordllpath"></a>AuthenticatorDllPath



| Constant Value | AuthenticatorDllPath                                                                                          |
|----------------|---------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ Espandi \_ SZ                                                                                               |
| Descrizione    | Percorso della DLL del metodo di autenticazione EAP. Ad esempio,% SystemRoot% \\ system32 \\ &lt; nome \_ di \_ dll &gt; . dll. |



 

## <a name="authenticatorfriendlyname"></a>AuthenticatorFriendlyName



| Constant Value | AuthenticatorFriendlyName                                                          |
|----------------|------------------------------------------------------------------------------------|
| Tipo           | REG \_ SZ                                                                            |
| Descrizione    | Stringa che contiene il nome descrittivo (visualizzazione) per il metodo di autenticazione EAP. |



 

## <a name="configclsid"></a>ConfigCLSID



| Constant Value | ConfigCLSID                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ SZ                                                                                                                               |
| Descrizione    | Stringa che contiene il GUID della classe di configurazione per questo metodo di autenticazione, nel formato {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX} |



 

## <a name="properties"></a>Proprietà



| Constant Value | Proprietà                                                                                                                                                  |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ DWORD                                                                                                                                                  |
| Descrizione    | I bit in DWORD sono impostati per indicare il supporto per la proprietà. Per un elenco dei valori supportati, vedere [**proprietà del metodo EAP**](eap-method-properties.md). |



 

## <a name="standalonesupported"></a>StandaloneSupported



| Constant Value | StandaloneSupported                                             |
|----------------|-----------------------------------------------------------------|
| Tipo           | REG \_ DWORD                                                      |
| Descrizione    | 0 se si tratta di un metodo di autenticazione autonomo; 1 in caso contrario. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Chiavi del registro di sistema del peer EAP](eap-peer-method-registry-keys.md)
</dt> <dt>

[Configurazione del registro di sistema per i tipi EAP espansi](registry-keys-for-eap-methods.md)
</dt> <dt>

[Uso di EAPHost](using-eap-host.md)
</dt> <dt>

[RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016)
</dt> </dl>

 

 




