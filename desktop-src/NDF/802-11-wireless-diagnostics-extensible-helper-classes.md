---
title: Classi helper estendibili di diagnostica wireless 802,11
description: L'infrastruttura di diagnostica wireless incorporata ha due punti di estensione. Supporto per l'helper ClassPurposeRevised Native Wi-Fi (RNWF) di helper ClassDiagnoses correlati a 802,11 estensioni di connettività.
ms.assetid: b54f836d-4fae-4e71-bf7b-af5a6e9e615c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bde49561c68044157c9d518571b8241c49dcf25
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104516633"
---
# <a name="80211-wireless-diagnostics-extensible-helper-classes"></a>Classi helper estendibili di diagnostica wireless 802,11

L'infrastruttura di diagnostica wireless incorporata ha due punti di estensione.

| Classe helper padre                                | Scopo                                                           |
|----------------------------------------------------|-------------------------------------------------------------------|
| Classe helper estendibile WiFi nativa (RNWF) modificata | Consente di diagnosticare i problemi relativi alle estensioni di connettività 802,11.       |
| Classe helper estendibile L2Security                 | Consente di diagnosticare i problemi relativi alle estensioni del protocollo di sicurezza di livello 2. |



 

> [!Note]  
> Una classe helper di terze parti deve eseguire la registrazione con entrambe le classi helper padre per assicurarsi che venga chiamata la classe di terze parti. Per ulteriori informazioni sulla registrazione, vedere la pagina relativa alla registrazione delle [estensioni di classe helper NDF](registering-ndf-helper-class-extensions.md).

 

## <a name="rnwf-extensible-helper-class"></a>Classe helper estendibile RNWF

Nome classe helper padre

``` syntax
Parent = L"RNWF Extensible Helper Class";
```

La classe helper estendibile RNWF (WiFi native) modificata è l'elemento padre per le classi helper di terze parti che diagnosticano i problemi correlati all'estensione di protocolli 802,11 utilizzati dal Wi-Fi nativo.

I due attributi chiave forniti dalla classe helper RNWF sono il GUID dell'interfaccia in cui si è verificato il problema e il contesto di connessione.

-   GUID interfaccia: questo attributo è denominato "ID interfaccia" ed è di tipo **al \_ GUID**.

-   Contesto di connessione: questo attributo è denominato ID di rete ed è di tipo in \_ \_ stringa ottetto. Questa stringa è in realtà un buffer della \_ \_ \_ struttura di ID WLAN WDIAG IHV definita in Wlanihv. h. Questa struttura viene definita come indicato di seguito.

    ``` syntax
#define WDIAG_IHV_WLAN_ID_FLAG_SECURITY_ENABLED               0x00000001
    typedef
    struct _WDIAG_IHV_WLAN_ID
    {
        WCHAR                        strProfileName [MS_MAX_PROFILE_NAME_LENGTH];
        DOT11_SSID                   Ssid;
        DOT11_BSS_TYPE               BssType;
        DWORD                        dwFlags;           // Flags defined above
        DWORD                        dwReasonCode;      // Set only when an applicable reason code is available
    }
    WDIAG_IHV_WLAN_ID, *PWDIAG_IHV_WLAN_ID;
    ```

> [!Note]  
> **WDIAG \_ La \_ \_ sicurezza del flag ID WLAN IHV \_ \_ \_ abilitato** è l'unico valore **dwFlags** possibile.

 

L'attributo corrispondente per la classe helper di terze parti deve corrispondere all'ID del servizio del modulo software corrispondente. Questo è lo stesso nome che la terza parte deve essere registrata nel registro di sistema. La diagnostica wireless eseguirà una query sull'ID servizio durante la sessione wireless in cui si è verificato il problema. Le informazioni verranno restituite a NDF, che determinerà se la classe helper di terze parti è presente e registrata, quindi la chiama.

Nella tabella seguente sono elencati gli attributi corrispondenti per la classe helper estensibile RNWF.



| Nome          | Type    | valore                         |
|---------------|---------|-------------------------------|
| DiagnosticsID | REG \_ SZ | \[\_Stringa GUID \_ DiagnosticsID |



 

## <a name="l2security-extensible-helper-class"></a>Classe helper estendibile L2Security

Nome classe helper padre

``` syntax
Parent = L"Extensible L2Sec Helper Class";
```

La classe helper Extensible Layer 2 Security (L2Security) è l'elemento padre per le classi helper di terze parti che diagnosticano i problemi relativi ai servizi e ai moduli software corrispondenti che sostituiscono la funzionalità di sicurezza di livello 2.

I due attributi chiave forniti dalla classe helper di sicurezza di livello 2 sono il GUID dell'interfaccia in cui si è verificato il problema e il contesto di connessione.

-   GUID interfaccia: questo attributo è denominato "ID interfaccia" ed è di tipo **al \_ GUID**.

-   Contesto di connessione: questo attributo è denominato ID di rete ed è di tipo in \_ \_ stringa ottetto. Questa stringa è in realtà un buffer della \_ \_ \_ struttura di ID WLAN WDIAG IHV definita in wlanihv. h. Questa struttura viene definita come indicato di seguito.

    ``` syntax
#define WDIAG_IHV_WLAN_ID_FLAG_SECURITY_ENABLED               0x00000001
    typedef
    struct _WDIAG_IHV_WLAN_ID
    {
        WCHAR                        strProfileName [MS_MAX_PROFILE_NAME_LENGTH];
        DOT11_SSID                   Ssid;
        DOT11_BSS_TYPE               BssType;
        DWORD                        dwFlags;           // Flags defined above
        DWORD                        dwReasonCode;      // Set only when an applicable reason code is available
    }
    WDIAG_IHV_WLAN_ID, *PWDIAG_IHV_WLAN_ID;
    ```

> [!Note]  
> **WDIAG \_ La \_ \_ sicurezza del flag ID WLAN IHV \_ \_ \_ abilitato** è l'unico valore **dwFlags** possibile.

 

L'attributo corrispondente per la classe helper di terze parti deve corrispondere all'ID del servizio del modulo software corrispondente. Questo è lo stesso nome che la terza parte deve essere registrata nel registro di sistema. La diagnostica wireless eseguirà una query sull'ID servizio durante la sessione wireless in cui si è verificato il problema. Le informazioni verranno restituite a NDF, che determinerà se la classe helper di terze parti è presente e registrata, quindi la chiama.

Nella tabella seguente sono elencati gli attributi corrispondenti per la classe di supporto estensibile di sicurezza di livello 2.



| Nome          | Type    | valore                         |
|---------------|---------|-------------------------------|
| DiagnosticsID | REG \_ SZ | \[\_Stringa GUID \_ DiagnosticsID |



 

## <a name="matching-attributes"></a>Attributi corrispondenti

**DiagnosticsID**

802,11 diagnostica wireless eseguirà una query sul *DiagnosticsID* dal servizio Wi-Fi nativo di base per verificare se sono installate e incluse nella connessione eventuali moduli di sicurezza o estensioni wireless di terze parti. La diagnostica senza fili fornirà quindi le ipotesi alle classi helper di terze parti usando *DiagnosticsID* come attributo corrispondente. Tutte le classi helper di terze parti devono essere incluse in e installate con il pacchetto driver associato. Il *DiagnosticsID* verrà definito nel file inf di miniport come chiave del registro di sistema nella direttiva [AddReg](https://msdn.microsoft.com/library/ms794514.aspx) .

``` syntax
HKR,Ndi\IHVExtensions, DiagnosticsID,0, "<Diagnostics ID GUID>"
```

Questa chiave definisce l'ID della classe helper wireless per il modulo software di terze parti. Questa chiave è facoltativa per il Framework di estendibilità, ma è necessaria se l'implementazione include una classe helper wireless IHV che si connette a NDF ed è in grado di diagnosticare i problemi di connettività correlati alle estensioni wireless o di sicurezza RNWF. Le classi helper MS WLAN Diagnostics eseguiranno una query su questo ID dal servizio configurazione automatica senza fili quando vengono installati i moduli IHV e forniranno questo ID come riferimento o attributo corrispondente a NDF durante una sessione di diagnostica in modo che NDF possa chiamare la classe helper wireless di terze parti appropriata quando necessario.

**\[\_Stringa GUID \_ DiagnosticsID\]**

Questo valore deve essere una stringa di tutte le lettere maiuscole. Ad esempio, "{12345678-9ABC-DEF0-1234-56789ABCDEF0}".

## <a name="scope-of-80211-wireless-diagnostics-helper-classes"></a>Ambito delle classi helper di diagnostica wireless 802,11

802,11 le classi helper di diagnostica wireless attualmente diagnosticano i problemi wireless nelle aree seguenti.

-   Eventuali problemi di connettività 802,11 tra cui 802,11 Association, 802,11 Authentication, 802,11 impostazioni di sicurezza relative agli standard 802,11 & protocolli supportati in modo nativo nel sistema operativo e problemi di prestazioni.
-   Problemi di sicurezza di livello 2 per quanto concerne le configurazioni 802.1 x e i problemi correlati all'autenticazione di livello 2 usando i metodi supportati in modo nativo in Windows Vista e Windows Server 2008.
-   Configurazione non corrispondente nelle impostazioni del profilo tra il client e il punto di accesso o l'infrastruttura e i servizi di rete.

802,11 le classi helper di diagnostica wireless attualmente non diagnosticano i problemi wireless nelle aree seguenti.

-   Problemi correlati alle estensioni 802,11 di terze parti, incluse le impostazioni del profilo o del driver correlate a tali estensioni.
-   Problemi relativi ai metodi EAP di terze parti.
-   Problemi del driver miniport wireless.
-   Qualsiasi protocollo di sicurezza 802,11 e di livello 2 o problemi relativi agli standard che non sono supportati in modo nativo.
-   Problemi a livello di sistema o di componente che potrebbero influisca sulla connettività wireless, ad esempio risparmio energia, spazio su disco insufficiente, condizioni di memoria e problemi hardware.

Inoltre, la diagnostica wireless 802,11 non analizza i case [**utilizzo del**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-highutilization) . I problemi di prestazioni wireless identificati verranno analizzati e segnalati come casi [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) .

 

 




