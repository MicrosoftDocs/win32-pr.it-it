---
title: Valori del Registro Authenticator metodo EAP
description: Informazioni sui valori del Registro Authenticator metodo EAP. Questi valori del Registro di sistema specifici sono necessari per i metodi dell'autenticatore EAP.
ms.assetid: 9374f9f7-b088-4e3a-ac96-8ccbeda87bb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1db88a910a40519533ffddae40c1e1cc04d36b62f3d3ad6543ddd4a2999373e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984311"
---
# <a name="eap-authenticator-method-registry-values"></a>Valori del Registro Authenticator metodo EAP

Per i metodi dell'autenticatore EAP sono necessari valori del Registro di sistema specifici.

## <a name="eap-authenticator-method-dll-paths"></a>Percorsi DLL Authenticator metodo EAP

Il percorso seguente specifica il percorso del Registro di sistema per le NORMALI DLL del metodo di autenticazione EAP.

**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ Methods \\ *&lt; AuthorId &gt;* \\ * &lt; EapTypeId&gt;***

Ad esempio, un percorso di registrazione di installazione del metodo di autenticazione EAP dato un **AuthorId** "311" (che indica che "Microsoft" è l'autore) e un **EapTypeId** di "40", viene visualizzato come segue.

**Metodi Eaphost dei servizi CCS del sistema HKLM \\ \\ \\ \\ \\ \\ 311 \\ 40**

Il percorso seguente specifica il percorso del Registro di sistema per le DLL estese del metodo di autenticazione EAP.

**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ Methods \\ *&lt; AuthorId &gt;* \\ 254 \\ *&lt; VendorId &gt;* \\ * &lt; VendorType&gt;***

Ad esempio, un percorso di registrazione di installazione del metodo di autenticazione EAP dato un **AuthorId** "311" (che indica che "Microsoft" è l'autore), un **VendorId** di "311" e un **EapTypeId** "40", viene visualizzato come segue.

**Metodi Eaphost dei servizi CCS del sistema HKLM \\ \\ \\ \\ \\ \\ 311 \\ 254 \\ 311 \\ 40**

> [!Note]  
> Per altre informazioni sull'allocazione dei tipi di metodo EAP, vedere la sezione 6.2 di [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).

 

## <a name="registry-values"></a>Valori del Registro di sistema

Sono necessari i valori del Registro di sistema del metodo di autenticazione seguenti.

-   [AuthenticatorDllPath](#authenticatordllpath)
-   [AuthenticatorFriendlyName](#authenticatorfriendlyname)

Oltre ai valori del Registro di sistema precedenti, è consigliabile il valore del Registro di sistema del metodo di autenticazione seguente.

-   [Proprietà](#properties)

I restanti valori del Registro di sistema del metodo di autenticazione sono facoltativi.

-   [ConfigCLSID](#configclsid)
-   [StandaloneSupported](#standalonesupported)

## <a name="authenticatordllpath"></a>AuthenticatorDllPath



| Constant Value | AuthenticatorDllPath                                                                                          |
|----------------|---------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ EXPAND \_ SZ                                                                                               |
| Descrizione    | Percorso della DLL del metodo di autenticazione EAP. Ad esempio, %SystemRoot% \\ system32 nome della \\ &lt; DLL \_ \_ &gt;.dll. |



 

## <a name="authenticatorfriendlyname"></a>AuthenticatorFriendlyName



| Constant Value | AuthenticatorFriendlyName                                                          |
|----------------|------------------------------------------------------------------------------------|
| Tipo           | REG \_ SZ                                                                            |
| Descrizione    | Stringa contenente il nome descrittivo (visualizzato) per il metodo di autenticazione EAP. |



 

## <a name="configclsid"></a>ConfigCLSID



| Constant Value | ConfigCLSID                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ SZ                                                                                                                               |
| Descrizione    | Stringa che contiene il GUID della classe di configurazione per questo metodo di autenticazione, nel formato {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX} |



 

## <a name="properties"></a>Proprietà



| Constant Value | Proprietà                                                                                                                                                  |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ DWORD                                                                                                                                                  |
| Descrizione    | I bit nella DWORD vengono impostati per indicare il supporto per la proprietà . Per un elenco dei valori supportati, vedere [**Proprietà del metodo EAP**](eap-method-properties.md). |



 

## <a name="standalonesupported"></a>StandaloneSupported



| Constant Value | StandaloneSupported                                             |
|----------------|-----------------------------------------------------------------|
| Tipo           | REG \_ DWORD                                                      |
| Descrizione    | 0 se si tratta di un metodo di autenticazione autonomo; 1 in caso non lo sia. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Chiavi del Registro di sistema dei metodi peer EAP](eap-peer-method-registry-keys.md)
</dt> <dt>

[Configurazione del Registro di sistema per i tipi EAP espansi](registry-keys-for-eap-methods.md)
</dt> <dt>

[Uso di EAPHost](using-eap-host.md)
</dt> <dt>

[RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016)
</dt> </dl>

 

 




