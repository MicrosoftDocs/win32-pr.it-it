---
description: Se si verifica un errore, WMI restituisce un codice di errore come valore HRESULT. Questi codici possono essere restituiti da script, applicazioni C++ o WMIC.
ms.assetid: b560f37c-da22-4745-8d1f-b27afdf572ec
ms.tgt_platform: multiple
title: Costanti di errore WMI (WbemCli. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e95db7220bdc9669716dbe19f5bf2f4e139dfe5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309754"
---
# <a name="wmi-error-constants"></a>Costanti di errore WMI

Se si verifica un errore, WMI restituisce un codice di errore come valore **HRESULT** . Questi codici possono essere restituiti da script, applicazioni C++ o [**wmic**](wmic.md).

> [!Note]
>
> La seguente documentazione è destinata agli sviluppatori e agli amministratori IT. Se si è un utente finale che ha riscontrato un messaggio di errore relativo a WMI, è necessario passare a [supporto tecnico Microsoft](https://support.microsoft.com/) e cercare il codice di errore visualizzato nel messaggio di errore. Per ulteriori informazioni sulla risoluzione dei problemi relativi agli script WMI e al servizio WMI, vedere [WMI non funziona](/previous-versions/tn-archive/ff406382(v=msdn.10)).
>
> Se WMI restituisce messaggi di errore, tenere presente che potrebbero non indicare problemi nel servizio WMI o nei provider WMI. Gli errori possono provenire in altre parti del sistema operativo e emergono come errori tramite WMI. In qualsiasi circostanza, non eliminare il repository WMI come prima azione perché l'eliminazione del repository può causare danni al sistema o alle applicazioni installate.
>
> Per ottenere ulteriori informazioni sull'origine del problema, è possibile scaricare ed eseguire lo strumento da riga di comando [utilità di diagnosi di WMI](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) diagnostica. Questo strumento genera un report che in genere può isolare l'origine del problema e fornire istruzioni su come risolverlo. Il report contribuisce inoltre ai servizi di supporto tecnico Microsoft. È possibile scaricare il Utilità di diagnosi di WMI [qui](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).

 

Alcuni metodi delle classi WMI possono restituire codici di errore di sistema e di rete (ad esempio, 64). È possibile controllare la definizione di questi tipi di codici di errore usando il comando **net helpmsg** nella finestra del prompt dei comandi. Ad esempio, il comando **net helpmsg 64** restituisce il messaggio: il nome di rete specificato non è più disponibile.

Nell'elenco seguente sono elencati alcuni intervalli comuni di errori.

<dl> <dt>

<span id="0x80041068_-_0x80041099"></span><span id="0X80041068_-_0X80041099"></span>0x80041068 - 0x80041099
</dt> <dd>

Errori che hanno origine in WMI.

Un'operazione WMI specifica non è riuscita a causa di

-   Un errore nella richiesta, ad esempio, una query WQL ha esito negativo o l'account non dispone delle autorizzazioni corrette.
-   Un problema di infrastruttura WMI, ad esempio la registrazione CIM o DCOM non corretta.

</dd> <dt>

<span id="0x8007xxxx"></span><span id="0X8007XXXX"></span>0x8007xxxx
</dt> <dd>

Errori originati nel sistema operativo di base. WMI può restituire questo tipo di errore a causa di un errore esterno, ad esempio un errore di sicurezza DCOM.

</dd> <dt>

<span id="0x80040xxx"></span><span id="0X80040XXX"></span>0x80040xxx
</dt> <dd>

Errori provenienti da DCOM. La configurazione DCOM per le operazioni in un computer remoto, ad esempio, potrebbe non essere corretta.

</dd> <dt>

<span id="0x8005xxxx"></span><span id="0X8005XXXX"></span>0x8005xxxx
</dt> <dd>

Errore originato da ADSI (Active Directory interfacce del servizio) o LDAP (Lightweight Directory Access Protocol), ad esempio, un errore di accesso Active Directory quando si utilizzano i provider di Active Directory WMI.

</dd> </dl>

Alcuni metodi delle classi WMI possono restituire codici di errore di sistema e di rete (ad esempio, 64). È possibile controllare la definizione di questi tipi di codici di errore usando il comando **net helpmsg** nella finestra del prompt dei comandi. Ad esempio, il comando **net helpmsg 64** restituisce il messaggio: il nome di rete specificato non è più disponibile. In C++ è possibile chiamare [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) e specificare **C: \\ Windows \\ system32 \\ WBEM \\wmiutils.dll** come modulo Message.

<dl> <dt>

<span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**WBEM \_ E \_ non riuscito**
</dt> <dd> <dl> <dt>

2147749889 (0x80041001)
</dt> <dt>



Chiamata non riuscita.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM \_ E \_ non \_ trovato**
</dt> <dd> <dl> <dt>

2147749890 (0x80041002)
</dt> <dt>



Impossibile trovare l'oggetto.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ACCESS_DENIED"></span><span id="wbem_e_access_denied"></span>**accesso a WBEM \_ E \_ \_ negato**
</dt> <dd> <dl> <dt>

2147749891 (0x80041003)
</dt> <dt>



L'utente corrente non dispone delle autorizzazioni necessarie per eseguire l'azione.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**\_errore del \_ provider WBEM E \_**
</dt> <dd> <dl> <dt>

2147749892 (0x80041004)
</dt> <dt>



Il provider ha avuto esito negativo in un momento diverso dall'inizializzazione.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**\_tipo WBEM E non \_ \_ corrispondente**
</dt> <dd> <dl> <dt>

2147749893 (0x80041005)
</dt> <dt>



Mancata corrispondenza del tipo.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**WBEM \_ E \_ \_ \_ memoria insufficiente**
</dt> <dd> <dl> <dt>

2147749894 (0x80041006)
</dt> <dt>



Memoria insufficiente per l'operazione.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_CONTEXT"></span><span id="wbem_e_invalid_context"></span>**\_contesto WBEM E \_ non valido \_**
</dt> <dd> <dl> <dt>

2147749895 (0x80041007)
</dt> <dt>



L'oggetto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) non è valido.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PARAMETER"></span><span id="wbem_e_invalid_parameter"></span>**\_parametro WBEM E \_ non valido \_**
</dt> <dd> <dl> <dt>

2147749896 (0x80041008)
</dt> <dt>



Uno dei parametri della chiamata non è corretto.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_AVAILABLE"></span><span id="wbem_e_not_available"></span>**WBEM \_ E \_ non \_ disponibile**
</dt> <dd> <dl> <dt>

2147749897 (0x80041009)
</dt> <dt>



La risorsa, in genere un server remoto, non è attualmente disponibile.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CRITICAL_ERROR"></span><span id="wbem_e_critical_error"></span>**WBEM \_ E \_ \_ errore critico**
</dt> <dd> <dl> <dt>

2147749898 (0x8004100A)
</dt> <dt>



Si è verificato un errore interno, critico e imprevisto. Segnalare l'errore al supporto tecnico Microsoft.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_STREAM"></span><span id="wbem_e_invalid_stream"></span>**\_flusso WBEM E \_ non valido \_**
</dt> <dd> <dl> <dt>

2147749899 (0x8004100B)
</dt> <dt>



Nel corso di una sessione remota uno o più pacchetti di rete erano danneggiati.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**WBEM \_ E \_ non \_ supportato**
</dt> <dd> <dl> <dt>

2147749900 (0x8004100C)
</dt> <dt>



Funzionalità o operazione non supportata.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_SUPERCLASS"></span><span id="wbem_e_invalid_superclass"></span>**superclasse WBEM \_ E \_ non valida \_**
</dt> <dd> <dl> <dt>

2147749901 (0x8004100D)
</dt> <dt>



Classe padre specificata non valida.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**\_ \_ spazio dei nomi WBEM E non valido \_**
</dt> <dd> <dl> <dt>

2147749902 (0x8004100E)
</dt> <dt>



Impossibile trovare lo spazio dei nomi specificato.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**\_oggetto WBEM E \_ non valido \_**
</dt> <dd> <dl> <dt>

2147749903 (0x8004100F)
</dt> <dt>



L'istanza specificata non è valida.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_CLASS"></span><span id="wbem_e_invalid_class"></span>**\_classe WBEM \_ E \_ classe non valida**
</dt> <dd> <dl> <dt>

2147749904 (0x80041010)
</dt> <dt>



La classe specificata non è valida.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_NOT_FOUND"></span><span id="wbem_e_provider_not_found"></span>**\_provider WBEM \_ E \_ non \_ trovato**
</dt> <dd> <dl> <dt>

2147749905 (0x80041011)
</dt> <dt>



Il provider a cui viene fatto riferimento nello schema non dispone di una registrazione corrispondente.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PROVIDER_REGISTRATION"></span><span id="wbem_e_invalid_provider_registration"></span>**\_registrazione del provider WBEM E \_ non valida \_ \_**
</dt> <dd> <dl> <dt>

2147749906
</dt> <dt>



Il provider a cui viene fatto riferimento nello schema ha una registrazione errata o incompleta.

Questo errore può essere causato da molte condizioni, incluse le seguenti:

-   Comando per [ \# lo spazio dei nomi pragma](pragma-namespace.md) mancante nel file Managed Object Format (MOF) usato per registrare il provider. Il provider può essere registrato nello spazio dei nomi WMI errato.
-   Errore durante il recupero della registrazione COM.
-   Il modello di hosting non è valido. Per altre informazioni, vedere [hosting e sicurezza del provider](provider-hosting-and-security.md).
-   Una classe specificata nella registrazione non è valida.
-   Impossibile creare un'istanza di o ereditare dalla classe [**\_ \_ Win32Provider**](--win32provider.md) per creare la registrazione del provider nel file MOF.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_LOAD_FAILURE"></span><span id="wbem_e_provider_load_failure"></span>**\_errore di \_ caricamento del provider WBEM E \_ \_**
</dt> <dd> <dl> <dt>

2147749907 (0x80041013)
</dt> <dt>



COM non può individuare un provider cui si fa riferimento nello schema.

Questo errore può essere causato da molte condizioni, incluse le seguenti:

-   Il provider utilizza una DLL WMI che non corrisponde al file con estensione lib utilizzato al momento della compilazione del provider.
-   La DLL del provider, o una qualsiasi DLL da cui dipende, è danneggiata.
-   Il provider non è riuscito a esportare [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver).
-   Il provider in-process non è stato registrato con il comando **regsvr32** .
-   Il provider out-of-process non è stato registrato con l'opzione **/regserver** . Ad esempio, **myprog.exe/regserver**.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**\_errore di \_ inizializzazione WBEM E \_**
</dt> <dd> <dl> <dt>

2147749908 (0x80041014)
</dt> <dt>



Impossibile inizializzare il componente, ad esempio un provider, per motivi interni.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TRANSPORT_FAILURE"></span><span id="wbem_e_transport_failure"></span>**\_errore di \_ trasporto WBEM E \_**
</dt> <dd> <dl> <dt>

2147749909 (0x80041015)
</dt> <dt>



Si è verificato un errore di rete che impedisce il normale funzionamento.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**\_operazione WBEM E \_ non valida \_**
</dt> <dd> <dl> <dt>

2147749910 (0x80041016)
</dt> <dt>



L'operazione richiesta non è valida. Questo errore si applica generalmente a tentativi non validi di eliminare classi o proprietà.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**\_query WBEM E \_ non valida \_**
</dt> <dd> <dl> <dt>

2147749911 (0x80041017)
</dt> <dt>



La sintassi della query non è valida.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**\_tipo di query WBEM E \_ non valido \_ \_**
</dt> <dd> <dl> <dt>

2147749912 (0x80041018)
</dt> <dt>



Il linguaggio di query richiesto non è supportato.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**WBEM \_ E \_ \_ esiste già**
</dt> <dd> <dl> <dt>

2147749913 (0x80041019)
</dt> <dt>



In un'operazione Put è stato specificato il flag **wbemChangeFlagCreateOnly** , ma l'istanza esiste già.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_override_not_allowed"></span>**\_sostituzione WBEM \_ E \_ non \_ consentita**
</dt> <dd> <dl> <dt>

2147749914 (0x8004101A)
</dt> <dt>



Non è possibile eseguire l'operazione di aggiunta su questo qualificatore perché l'oggetto proprietario non consente le sostituzioni.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPAGATED_QUALIFIER"></span><span id="wbem_e_propagated_qualifier"></span>**\_ \_ qualificatore WBEM E propagato \_**
</dt> <dd> <dl> <dt>

2147749915 (0x8004101B)
</dt> <dt>



L'utente ha tentato di eliminare un qualificatore non di proprietà. Il qualificatore è stato ereditato da una classe padre.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPAGATED_PROPERTY"></span><span id="wbem_e_propagated_property"></span>**\_Proprietà WBEM E \_ propagata \_**
</dt> <dd> <dl> <dt>

2147749916 (0x8004101C)
</dt> <dt>



L'utente ha tentato di eliminare una proprietà che non possedeva. La proprietà è stata ereditata da una classe padre.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNEXPECTED"></span><span id="wbem_e_unexpected"></span>**WBEM \_ E \_ imprevisto**
</dt> <dd> <dl> <dt>

2147749917 (0x8004101D)
</dt> <dt>



Il client ha eseguito una sequenza di chiamate imprevista e non valida, ad esempio la chiamata di [**EndEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-endenumeration) prima della chiamata a [**BeginEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-beginenumeration).


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ILLEGAL_OPERATION"></span><span id="wbem_e_illegal_operation"></span>**\_operazione WBEM E non \_ valida \_**
</dt> <dd> <dl> <dt>

2147749918 (0x8004101E)
</dt> <dt>



L'utente ha richiesto un'operazione non valida, ad esempio la generazione di una classe da un'istanza.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_BE_KEY"></span><span id="wbem_e_cannot_be_key"></span>**WBEM \_ E \_ non può \_ essere una \_ chiave**
</dt> <dd> <dl> <dt>

2147749919 (0x8004101F)
</dt> <dt>



Tentativo non valido di specificare un qualificatore di chiave su una proprietà che non può essere una chiave. Le chiavi sono specificate nella definizione della classe per un oggetto e non possono essere alterate per singole istanze.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INCOMPLETE_CLASS"></span><span id="wbem_e_incomplete_class"></span>**\_classe WBEM E \_ incompleta \_**
</dt> <dd> <dl> <dt>

2147749920 (0x80041020)
</dt> <dt>



L'oggetto corrente non è una definizione di classe valida. Il valore è incompleto o non è stato registrato con WMI mediante [**SWbemObject. put \_**](swbemobject-put-.md).


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**\_sintassi WBEM E \_ non valida \_**
</dt> <dd> <dl> <dt>

2147749921 (0x80041021)
</dt> <dt>



La sintassi della query non è valida.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NONDECORATED_OBJECT"></span><span id="wbem_e_nondecorated_object"></span>**WBEM \_ E \_ oggetto non decorato \_**
</dt> <dd> <dl> <dt>

2147749922 (0x80041022)
</dt> <dt>



Riservato per utilizzi futuri.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**WBEM \_ E \_ sola lettura \_**
</dt> <dd> <dl> <dt>

2147749923 (0x80041023)
</dt> <dt>



È stato effettuato un tentativo di modificare una proprietà di sola lettura.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**il \_ provider WBEM E \_ \_ non è \_ in grado di supportare**
</dt> <dd> <dl> <dt>

2147749924 (0x80041024)
</dt> <dt>



Il provider non è in grado di eseguire l'operazione richiesta. Questo può includere una query troppo complessa, il recupero di un'istanza, la creazione o l'aggiornamento di una classe, l'eliminazione di una classe o l'enumerazione di una classe.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CLASS_HAS_CHILDREN"></span><span id="wbem_e_class_has_children"></span>**WBEM \_ E \_ classe \_ con \_ elementi figlio**
</dt> <dd> <dl> <dt>

2147749925 (0x80041025)
</dt> <dt>



È stato effettuato un tentativo di apportare una modifica che invalida una sottoclasse.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CLASS_HAS_INSTANCES"></span><span id="wbem_e_class_has_instances"></span>**\_classe WBEM \_ E \_ con \_ istanze**
</dt> <dd> <dl> <dt>

2147749926 (0x80041026)
</dt> <dt>



È stato effettuato un tentativo di eliminare o modificare una classe con istanze.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_QUERY_NOT_IMPLEMENTED"></span><span id="wbem_e_query_not_implemented"></span>**\_query WBEM \_ E \_ non \_ implementata**
</dt> <dd> <dl> <dt>

2147749927 (0x80041027)
</dt> <dt>



Riservato per utilizzi futuri.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM \_ E \_ null non valido \_**
</dt> <dd> <dl> <dt>

2147749928 (0x80041028)
</dt> <dt>



Il valore Nothing/**null** è stato specificato per una proprietà che deve avere un valore, ad esempio uno contrassegnato da un qualificatore di [**chiave**](key-qualifier.md), [**indicizzato**](optional-qualifiers.md)o **Not \_ null** .


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUALIFIER_TYPE"></span><span id="wbem_e_invalid_qualifier_type"></span>**\_tipo di \_ \_ qualificatore WBEM E non valido \_**
</dt> <dd> <dl> <dt>

2147749929 (0x80041029)
</dt> <dt>



È stato specificato il valore Variant per un qualificatore che non è un tipo di qualificatore valido.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PROPERTY_TYPE"></span><span id="wbem_e_invalid_property_type"></span>**\_tipo di proprietà WBEM E \_ non valido \_ \_**
</dt> <dd> <dl> <dt>

2147749930 (0x8004102A)
</dt> <dt>



Il tipo CIM specificato per una proprietà non è valido.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**\_valore WBEM E non compreso nell' \_ \_ \_ \_ intervallo**
</dt> <dd> <dl> <dt>

2147749931 (0x8004102B)
</dt> <dt>



La richiesta è stata eseguita con un valore esterno all'intervallo o non è compatibile con il tipo.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_BE_SINGLETON"></span><span id="wbem_e_cannot_be_singleton"></span>**WBEM \_ E \_ non può \_ essere \_ singleton**
</dt> <dd> <dl> <dt>

2147749932 (0x8004102C)
</dt> <dt>



È stato effettuato un tentativo non valido di creare un singleton della classe, ad esempio quando la classe è derivata da una classe non singleton.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_CIM_TYPE"></span><span id="wbem_e_invalid_cim_type"></span>**WBEM \_ E \_ \_ tipo CIM non valido \_**
</dt> <dd> <dl> <dt>

2147749933 (0x8004102D)
</dt> <dt>



Il tipo CIM specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**WBEM \_ E \_ metodo non valido \_**
</dt> <dd> <dl> <dt>

2147749934 (0x8004102E)
</dt> <dt>



Il metodo richiesto non è disponibile.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**\_parametri del metodo WBEM E \_ non validi \_ \_**
</dt> <dd> <dl> <dt>

2147749935 (0x8004102F)
</dt> <dt>



I parametri forniti per il metodo non sono validi.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_SYSTEM_PROPERTY"></span><span id="wbem_e_system_property"></span>**\_proprietà di \_ sistema WBEM E \_**
</dt> <dd> <dl> <dt>

2147749936 (0x80041030)
</dt> <dt>



Si è verificato un tentativo di ottenere qualificatori su una proprietà di sistema.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PROPERTY"></span><span id="wbem_e_invalid_property"></span>**\_Proprietà WBEM E \_ non valida \_**
</dt> <dd> <dl> <dt>

2147749937 (0x80041031)
</dt> <dt>



Il tipo di proprietà non è riconosciuto.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CALL_CANCELLED"></span><span id="wbem_e_call_cancelled"></span>**\_chiamata WBEM \_ E \_ annullata**
</dt> <dd> <dl> <dt>

2147749938 (0x80041032)
</dt> <dt>



Il processo asincrono è stato annullato internamente o dall'utente. Si noti che a causa dell'intervallo e della natura dell'operazione asincrona, è possibile che l'operazione non sia stata effettivamente annullata.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_SHUTTING_DOWN"></span><span id="wbem_e_shutting_down"></span>**chiusura di WBEM \_ E \_ \_**
</dt> <dd> <dl> <dt>

2147749939 (0x80041033)
</dt> <dt>



L'utente ha richiesto un'operazione mentre è in corso l'arresto di WMI.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPAGATED_METHOD"></span><span id="wbem_e_propagated_method"></span>**\_ \_ Metodo propagato WBEM \_ E**
</dt> <dd> <dl> <dt>

2147749940 (0x80041034)
</dt> <dt>



È stato effettuato un tentativo di riutilizzare un nome di metodo esistente da una classe padre e le firme non corrispondono.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNSUPPORTED_PARAMETER"></span><span id="wbem_e_unsupported_parameter"></span>**\_parametro WBEM E non \_ supportato \_**
</dt> <dd> <dl> <dt>

2147749941 (0x80041035)
</dt> <dt>



Uno o più valori di parametro, come un testo della query, è troppo complesso o non è supportato. Per questo motivo, è necessario ripetere l'operazione con parametri più semplici.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MISSING_PARAMETER_ID"></span><span id="wbem_e_missing_parameter_id"></span>**WBEM \_ E \_ \_ ID parametro \_ mancante**
</dt> <dd> <dl> <dt>

2147749942 (0x80041036)
</dt> <dt>



Il parametro non è presente nella chiamata al metodo.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PARAMETER_ID"></span><span id="wbem_e_invalid_parameter_id"></span>**\_ID parametro WBEM E \_ non valido \_ \_**
</dt> <dd> <dl> <dt>

2147749943 (0x80041037)
</dt> <dt>



Il parametro del metodo ha un qualificatore [**ID**](standard-wmi-qualifiers.md) non valido.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NONCONSECUTIVE_PARAMETER_IDS"></span><span id="wbem_e_nonconsecutive_parameter_ids"></span>**\_ID di parametro WBEM E non \_ consecutivi \_ \_**
</dt> <dd> <dl> <dt>

2147749944 (0x80041038)
</dt> <dt>



Uno o più parametri del metodo hanno qualificatori [**ID**](standard-wmi-qualifiers.md) fuori sequenza.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PARAMETER_ID_ON_RETVAL"></span><span id="wbem_e_parameter_id_on_retval"></span>**\_ \_ ID parametro WBEM \_ E \_ in \_ retval**
</dt> <dd> <dl> <dt>

2147749945 (0x80041039)
</dt> <dt>



Il valore restituito per un metodo ha un qualificatore [**ID**](standard-wmi-qualifiers.md) .


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**\_percorso dell'oggetto WBEM E \_ non valido \_ \_**
</dt> <dd> <dl> <dt>

2147749946 (0x8004103A)
</dt> <dt>



Il percorso dell'oggetto specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_OUT_OF_DISK_SPACE"></span><span id="wbem_e_out_of_disk_space"></span>**\_ \_ \_ \_ spazio disponibile su disco WBEM E esaurito \_**
</dt> <dd> <dl> <dt>

2147749947 (0x8004103B)
</dt> <dt>



Lo spazio su disco è esaurito o è stato raggiunto il limite di 4 GB per il repository WMI (repository CIM).


</dt> </dl> </dd> <dt>

<span id="WBEM_E_BUFFER_TOO_SMALL"></span><span id="wbem_e_buffer_too_small"></span>**\_buffer WBEM \_ E \_ troppo \_ piccolo**
</dt> <dd> <dl> <dt>

2147749948 (0x8004103C)
</dt> <dt>



Il buffer fornito è troppo piccolo per conservare tutti gli oggetti nell'enumeratore o per leggere una proprietà di stringa.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNSUPPORTED_PUT_EXTENSION"></span><span id="wbem_e_unsupported_put_extension"></span>**WBEM \_ E \_ \_ put Extension non supportata \_**
</dt> <dd> <dl> <dt>

2147749949 (0x8004103D)
</dt> <dt>



Il provider non supporta l'operazione PUT richiesta.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNKNOWN_OBJECT_TYPE"></span><span id="wbem_e_unknown_object_type"></span>**WBEM \_ E \_ \_ tipo di oggetto sconosciuto \_**
</dt> <dd> <dl> <dt>

2147749950 (0x8004103E)
</dt> <dt>



Rilevato oggetto con tipo o versione non corretta durante il marshalling.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNKNOWN_PACKET_TYPE"></span><span id="wbem_e_unknown_packet_type"></span>**\_tipo di pacchetto WBEM E \_ sconosciuto \_ \_**
</dt> <dd> <dl> <dt>

2147749951 (0x8004103F)
</dt> <dt>



È stato rilevato un pacchetto con un tipo o una versione non corretta durante il marshalling.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MARSHAL_VERSION_MISMATCH"></span><span id="wbem_e_marshal_version_mismatch"></span>**\_versione del marshalling E di WBEM non \_ \_ \_ corrispondente**
</dt> <dd> <dl> <dt>

2147749952 (0x80041040)
</dt> <dt>



La versione del pacchetto non è supportata.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MARSHAL_INVALID_SIGNATURE"></span><span id="wbem_e_marshal_invalid_signature"></span>**\_firma del \_ marshalling E marshalling \_ non valido \_**
</dt> <dd> <dl> <dt>

2147749953 (0x80041041)
</dt> <dt>



Il pacchetto sembra danneggiato.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUALIFIER"></span><span id="wbem_e_invalid_qualifier"></span>**\_ \_ qualificatore WBEM E non valido \_**
</dt> <dd> <dl> <dt>

2147749954 (0x80041042)
</dt> <dt>



È stato effettuato un tentativo di mancata corrispondenza dei qualificatori, ad esempio inserendo \[ \] la chiave su un oggetto anziché una proprietà.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_DUPLICATE_PARAMETER"></span><span id="wbem_e_invalid_duplicate_parameter"></span>**\_ \_ parametro non valido per WBEM E \_ duplicato \_**
</dt> <dd> <dl> <dt>

2147749955 (0x80041043)
</dt> <dt>



Il parametro duplicato è stato dichiarato in un metodo CIM.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TOO_MUCH_DATA"></span><span id="wbem_e_too_much_data"></span>**WBEM \_ E \_ troppa \_ quantità di \_ dati**
</dt> <dd> <dl> <dt>

2147749956 (0x80041044)
</dt> <dt>



Riservato per utilizzi futuri.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_SERVER_TOO_BUSY"></span><span id="wbem_e_server_too_busy"></span>**WBEM \_ E \_ server \_ troppo \_ occupato**
</dt> <dd> <dl> <dt>

2147749957 (0x80041045)
</dt> <dt>



La chiamata a [**IWbemObjectSink:: indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) non è riuscita. Il provider può rigenerare l'evento.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_FLAVOR"></span><span id="wbem_e_invalid_flavor"></span>**versione WBEM \_ E \_ non valida \_**
</dt> <dd> <dl> <dt>

2147749958 (0x80041046)
</dt> <dt>



La versione del qualificatore specificata non è valida.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CIRCULAR_REFERENCE"></span><span id="wbem_e_circular_reference"></span>**\_ \_ riferimento circolare WBEM \_ E**
</dt> <dd> <dl> <dt>

2147749959 (0x80041047)
</dt> <dt>



È stato effettuato un tentativo di creare un riferimento circolare (ad esempio, derivando una classe da se stessa).


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNSUPPORTED_CLASS_UPDATE"></span><span id="wbem_e_unsupported_class_update"></span>**WBEM \_ E \_ aggiornamento della classe non supportato \_ \_**
</dt> <dd> <dl> <dt>

2147749960 (0x80041048)
</dt> <dt>



La classe specificata non è supportata.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_CHANGE_KEY_INHERITANCE"></span><span id="wbem_e_cannot_change_key_inheritance"></span>**WBEM \_ E \_ non è possibile \_ modificare l' \_ ereditarietà della chiave \_**
</dt> <dd> <dl> <dt>

2147749961 (0x80041049)
</dt> <dt>



È stato effettuato un tentativo di modificare una chiave quando le istanze o le sottoclassi usano già la chiave.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_CHANGE_INDEX_INHERITANCE"></span><span id="wbem_e_cannot_change_index_inheritance"></span>**WBEM \_ E \_ non può \_ modificare l' \_ ereditarietà degli indici \_**
</dt> <dd> <dl> <dt>

2147749968 (0x80041050)
</dt> <dt>



È stato effettuato un tentativo di modificare un indice quando le istanze o le sottoclassi usano già l'indice.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TOO_MANY_PROPERTIES"></span><span id="wbem_e_too_many_properties"></span>**WBEM \_ E \_ troppe \_ \_ Proprietà**
</dt> <dd> <dl> <dt>

2147749969 (0x80041051)
</dt> <dt>



È stato effettuato un tentativo di creare un numero di proprietà maggiore di quello supportato dalla versione corrente della classe.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UPDATE_TYPE_MISMATCH"></span><span id="wbem_e_update_type_mismatch"></span>**\_tipo di aggiornamento WBEM E non \_ \_ \_ corrispondente**
</dt> <dd> <dl> <dt>

2147749970 (0x80041052)
</dt> <dt>



La proprietà è stata ridefinita con un tipo in conflitto in una classe derivata.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UPDATE_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_update_override_not_allowed"></span>**\_sostituzione degli aggiornamenti WBEM E \_ \_ \_ non \_ consentita**
</dt> <dd> <dl> <dt>

2147749971 (0x80041053)
</dt> <dt>



Tentativo eseguito in una classe derivata per eseguire l'override di un qualificatore che non può essere sottoposto a override.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UPDATE_PROPAGATED_METHOD"></span><span id="wbem_e_update_propagated_method"></span>**\_ \_ \_ Metodo propagato WBEM E Update \_**
</dt> <dd> <dl> <dt>

2147749972 (0x80041054)
</dt> <dt>



Il metodo è stato nuovamente dichiarato con una firma in conflitto in una classe derivata.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_METHOD_NOT_IMPLEMENTED"></span><span id="wbem_e_method_not_implemented"></span>**\_Metodo WBEM \_ E \_ non \_ implementato**
</dt> <dd> <dl> <dt>

2147749973 (0x80041055)
</dt> <dt>



È stato effettuato un tentativo di eseguire un metodo non contrassegnato con \[ implementato \] in una classe rilevante.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_METHOD_DISABLED"></span><span id="wbem_e_method_disabled"></span>**WBEM \_ E \_ metodo \_ disabilitato**
</dt> <dd> <dl> <dt>


</dt> <dt>



È stato effettuato un tentativo di eseguire un metodo contrassegnato con \[ disabilitato \] .


</dt> </dl> </dd> <dt>

<span id="WBEM_E_REFRESHER_BUSY"></span><span id="wbem_e_refresher_busy"></span>**\_aggiornamento WBEM E \_ \_ occupato**
</dt> <dd> <dl> <dt>

2147749975 (0x80041057)
</dt> <dt>



Il servizio di aggiornamento è occupato con un'altra operazione.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNPARSABLE_QUERY"></span><span id="wbem_e_unparsable_query"></span>**\_query WBEM E non \_ analizzabile \_**
</dt> <dd> <dl> <dt>

2147749976 (0x80041058)
</dt> <dt>



La sintassi della query di filtro non è valida.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_EVENT_CLASS"></span><span id="wbem_e_not_event_class"></span>**WBEM \_ E \_ Not \_ - \_ classe di evento**
</dt> <dd> <dl> <dt>

2147749977 (0x80041059)
</dt> <dt>



La clausola from di una query di filtro fa riferimento a una classe che non è una classe di evento (non derivata da un [**\_ \_ evento**](--event.md)).


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MISSING_GROUP_WITHIN"></span><span id="wbem_e_missing_group_within"></span>**WBEM \_ E \_ \_ gruppo mancante \_ entro**
</dt> <dd> <dl> <dt>

2147749978 (0x8004105A)
</dt> <dt>



È stata utilizzata una clausola GROUP BY senza la corrispondente clausola GROUP WITHIN.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MISSING_AGGREGATION_LIST"></span><span id="wbem_e_missing_aggregation_list"></span>**WBEM \_ E \_ \_ elenco di aggregazioni mancanti \_**
</dt> <dd> <dl> <dt>

2147749979 (0x8004105B)
</dt> <dt>



È stata utilizzata una clausola GROUP BY. L'aggregazione di tutte le proprietà non è supportata.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPERTY_NOT_AN_OBJECT"></span><span id="wbem_e_property_not_an_object"></span>**\_Proprietà WBEM E \_ non è \_ \_ un \_ oggetto**
</dt> <dd> <dl> <dt>

2147749980 (0x8004105C)
</dt> <dt>



È stata utilizzata la notazione del punto in una proprietà che non è un oggetto incorporato.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_AGGREGATING_BY_OBJECT"></span><span id="wbem_e_aggregating_by_object"></span>**WBEM \_ E \_ aggregazione \_ per \_ oggetto**
</dt> <dd> <dl> <dt>

2147749981 (0x8004105D)
</dt> <dt>



Una clausola GROUP BY fa riferimento a una proprietà che è un oggetto incorporato senza l'utilizzo della notazione del punto.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNINTERPRETABLE_PROVIDER_QUERY"></span><span id="wbem_e_uninterpretable_provider_query"></span>**\_query del provider WBEM E non \_ interpretabile \_ \_**
</dt> <dd> <dl> <dt>

2147749983 (0x8004105F)
</dt> <dt>



La query di registrazione del provider di eventi ([**\_ \_ EventProviderRegistration**](--eventproviderregistration.md)) non ha specificato le classi per cui sono stati forniti gli eventi.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_BACKUP_RESTORE_WINMGMT_RUNNING"></span><span id="wbem_e_backup_restore_winmgmt_running"></span>**WBEM \_ E \_ backup \_ Restore \_ WinMgmt \_ in esecuzione**
</dt> <dd> <dl> <dt>

2147749984 (0x80041060)
</dt> <dt>



È stata effettuata una richiesta per eseguire il backup o il ripristino del repository mentre era usato da WinMgmt.exe o dal processo SVCHOST che contiene il servizio WMI.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_QUEUE_OVERFLOW"></span><span id="wbem_e_queue_overflow"></span>**\_ \_ overflow coda WBEM \_ E**
</dt> <dd> <dl> <dt>

2147749985 (0x80041061)
</dt> <dt>



Overflow della coda di recapito asincrono causato da un consumer di eventi troppo lento.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PRIVILEGE_NOT_HELD"></span><span id="wbem_e_privilege_not_held"></span>**il \_ privilegio WBEM E non è stato \_ \_ \_ mantenuto**
</dt> <dd> <dl> <dt>

2147749986 (0x80041062)
</dt> <dt>



L'operazione non è riuscita perché il client non dispone dei privilegi di sicurezza necessari.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OPERATOR"></span><span id="wbem_e_invalid_operator"></span>**\_operatore WBEM E \_ non valido \_**
</dt> <dd> <dl> <dt>

2147749987 (0x80041063)
</dt> <dt>



Operatore non valido per questo tipo di proprietà.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_LOCAL_CREDENTIALS"></span><span id="wbem_e_local_credentials"></span>**\_ \_ credenziali locali E \_ WBEM**
</dt> <dd> <dl> <dt>

2147749988 (0x80041064)
</dt> <dt>



L'utente ha specificato un nome utente/password/autorità in una connessione locale. L'utente deve usare un nome utente/password vuoto e fare affidamento sulla sicurezza predefinita.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_BE_ABSTRACT"></span><span id="wbem_e_cannot_be_abstract"></span>**WBEM \_ E \_ non può \_ essere \_ astratto**
</dt> <dd> <dl> <dt>

2147749989 (0x80041065)
</dt> <dt>



La classe è stata creata in modo astratto quando la relativa classe padre non è astratta.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_AMENDED_OBJECT"></span><span id="wbem_e_amended_object"></span>**WBEM \_ E \_ \_ oggetto modificato**
</dt> <dd> <dl> <dt>

2147749990 (0x80041066)
</dt> <dt>



L'oggetto modificato è stato scritto senza che il **flag WBEM usi il flag dei \_ \_ \_ \_ qualificatori modificati** specificato.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CLIENT_TOO_SLOW"></span><span id="wbem_e_client_too_slow"></span>**\_client WBEM \_ E \_ troppo \_ lento**
</dt> <dd> <dl> <dt>

2147749991 (0x80041067)
</dt> <dt>



Il client non ha recuperato gli oggetti in modo sufficientemente rapido da un'enumerazione. Questa costante viene restituita quando un client crea un oggetto di enumerazione, ma non recupera gli oggetti dall'enumeratore in modo tempestivo, causando il backup delle cache degli oggetti dell'enumeratore.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NULL_SECURITY_DESCRIPTOR"></span><span id="wbem_e_null_security_descriptor"></span>**\_descrittore di sicurezza WBEM E \_ null \_ \_**
</dt> <dd> <dl> <dt>

2147749992 (0x80041068)
</dt> <dt>



È stato utilizzato il descrittore di sicurezza null.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TIMED_OUT"></span><span id="wbem_e_timed_out"></span>**timeout di WBEM \_ E \_ \_**
</dt> <dd> <dl> <dt>

2147749993 (0x80041069)
</dt> <dt>



Timeout dell'operazione.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_ASSOCIATION"></span><span id="wbem_e_invalid_association"></span>**\_associazione WBEM E \_ non valida \_**
</dt> <dd> <dl> <dt>

2147749994
</dt> <dt>



Associazione non valida.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_AMBIGUOUS_OPERATION"></span><span id="wbem_e_ambiguous_operation"></span>**\_operazione WBEM E \_ ambigua \_**
</dt> <dd> <dl> <dt>

2147749995 (0x8004106B)
</dt> <dt>



L'operazione è ambigua.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_QUOTA_VIOLATION"></span><span id="wbem_e_quota_violation"></span>**\_violazione della \_ quota \_ E di WBEM**
</dt> <dd> <dl> <dt>

2147749996 (0x8004106C)
</dt> <dt>



WMI sta occupando troppa memoria. Questo problema può essere causato dalla disponibilità di memoria insufficiente o da un utilizzo eccessivo della memoria da WMI.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TRANSACTION_CONFLICT"></span><span id="wbem_e_transaction_conflict"></span>**\_conflitto di \_ transazioni WBEM E \_**
</dt> <dd> <dl> <dt>

2147749997 (0x8004106D)
</dt> <dt>



L'operazione ha causato un conflitto di transazioni.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_FORCED_ROLLBACK"></span><span id="wbem_e_forced_rollback"></span>**\_rollback E \_ forzato di WBEM \_**
</dt> <dd> <dl> <dt>

2147749998 (0x8004106E)
</dt> <dt>



Transazione forzata un rollback.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNSUPPORTED_LOCALE"></span><span id="wbem_e_unsupported_locale"></span>**WBEM \_ E \_ \_ impostazioni locali non supportate**
</dt> <dd> <dl> <dt>

2147749999 (0x8004106F)
</dt> <dt>



Le impostazioni locali utilizzate nella chiamata non sono supportate.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_HANDLE_OUT_OF_DATE"></span><span id="wbem_e_handle_out_of_date"></span>**WBEM \_ E \_ handle \_ non \_ \_ aggiornati**
</dt> <dd> <dl> <dt>

2147750000 (0x80041070)
</dt> <dt>



Handle di oggetto non aggiornato.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CONNECTION_FAILED"></span><span id="wbem_e_connection_failed"></span>**\_connessione WBEM \_ E \_ non riuscita**
</dt> <dd> <dl> <dt>

2147750001 (0x80041071)
</dt> <dt>



Connessione al database SQL non riuscita.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_HANDLE_REQUEST"></span><span id="wbem_e_invalid_handle_request"></span>**\_richiesta di \_ handle non valida per WBEM E \_ \_**
</dt> <dd> <dl> <dt>

2147750002 (0x80041072)
</dt> <dt>



La richiesta dell'handle non è valida.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPERTY_NAME_TOO_WIDE"></span><span id="wbem_e_property_name_too_wide"></span>**\_nome della proprietà WBEM E \_ \_ \_ troppo \_ ampio**
</dt> <dd> <dl> <dt>

2147750003 (0x80041073)
</dt> <dt>



Il nome della proprietà contiene più di 255 caratteri.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CLASS_NAME_TOO_WIDE"></span><span id="wbem_e_class_name_too_wide"></span>**il \_ nome della classe WBEM E è \_ \_ \_ troppo \_ ampio**
</dt> <dd> <dl> <dt>

2147750004 (0x80041074)
</dt> <dt>



Il nome della classe contiene più di 255 caratteri.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_METHOD_NAME_TOO_WIDE"></span><span id="wbem_e_method_name_too_wide"></span>**\_nome del metodo WBEM E \_ \_ \_ troppo \_ ampio**
</dt> <dd> <dl> <dt>

2147750005 (0x80041075)
</dt> <dt>



Il nome del metodo contiene più di 255 caratteri.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_QUALIFIER_NAME_TOO_WIDE"></span><span id="wbem_e_qualifier_name_too_wide"></span>**\_nome del \_ qualificatore WBEM E \_ \_ troppo \_ ampio**
</dt> <dd> <dl> <dt>

2147750006 (0x80041076)
</dt> <dt>



Il nome del qualificatore contiene più di 255 caratteri.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_RERUN_COMMAND"></span><span id="wbem_e_rerun_command"></span>**\_ \_ comando Riesegui WBEM E \_**
</dt> <dd> <dl> <dt>

2147750007 (0x80041077)
</dt> <dt>



È necessario eseguire di nuovo il comando SQL perché in SQL è presente un deadlock. Questa operazione può essere restituita solo quando i dati vengono archiviati in un database SQL.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_DATABASE_VER_MISMATCH"></span><span id="wbem_e_database_ver_mismatch"></span>**non \_ corrispondenza del database WBEM E \_ \_ ver \_**
</dt> <dd> <dl> <dt>

2147750008 (0x80041078)
</dt> <dt>



La versione del database non corrisponde alla versione elaborata dal driver del repository.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_VETO_DELETE"></span><span id="wbem_e_veto_delete"></span>**WBEM \_ E \_ veto \_ Delete**
</dt> <dd> <dl> <dt>

2147750009 (0x80041079)
</dt> <dt>



WMI non è in grado di eseguire l'operazione di eliminazione perché il provider non lo consente.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_VETO_PUT"></span><span id="wbem_e_veto_put"></span>**WBEM \_ E \_ veto \_ put**
</dt> <dd> <dl> <dt>

2147750010 (0x8004107A)
</dt> <dt>



WMI non è in grado di eseguire l'operazione Put perché il provider non lo consente.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_LOCALE"></span><span id="wbem_e_invalid_locale"></span>**\_ \_ impostazioni locali non valide per WBEM E \_**
</dt> <dd> <dl> <dt>

2147750016 (0x80041080)
</dt> <dt>



L'identificatore delle impostazioni locali specificato non è valido per l'operazione.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_SUSPENDED"></span><span id="wbem_e_provider_suspended"></span>**\_provider WBEM \_ E \_ sospeso**
</dt> <dd> <dl> <dt>

2147750017 (0x80041081)
</dt> <dt>



Il provider è sospeso.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_SYNCHRONIZATION_REQUIRED"></span><span id="wbem_e_synchronization_required"></span>**\_sincronizzazione WBEM \_ E \_ necessaria**
</dt> <dd> <dl> <dt>

2147750018 (0x80041082)
</dt> <dt>



L'oggetto deve essere scritto nel repository WMI e recuperato di nuovo prima che l'operazione richiesta possa essere eseguita correttamente. Questa costante viene restituita quando è necessario eseguire il commit e il recupero di un oggetto per visualizzare il valore della proprietà.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NO_SCHEMA"></span><span id="wbem_e_no_schema"></span>**WBEM \_ E \_ nessun \_ schema**
</dt> <dd> <dl> <dt>

2147750019 (0x80041083)
</dt> <dt>



Non è possibile completare l'operazione. non è disponibile alcuno schema.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_ALREADY_REGISTERED"></span><span id="wbem_e_provider_already_registered"></span>**\_provider WBEM \_ E \_ già \_ registrato**
</dt> <dd> <dl> <dt>

02147750020 (0x119FD010)
</dt> <dt>



Impossibile registrare il provider perché è già registrato.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_NOT_REGISTERED"></span><span id="wbem_e_provider_not_registered"></span>**\_provider WBEM \_ E \_ non \_ registrato**
</dt> <dd> <dl> <dt>

2147750021 (0x80041085)
</dt> <dt>



Il provider non è registrato.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_FATAL_TRANSPORT_ERROR"></span><span id="wbem_e_fatal_transport_error"></span>**\_errore di trasporto WBEM E \_ irreversibile \_ \_**
</dt> <dd> <dl> <dt>

2147750022 (0x80041086)
</dt> <dt>



Si è verificato un errore di trasporto irreversibile.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ENCRYPTED_CONNECTION_REQUIRED"></span><span id="wbem_e_encrypted_connection_required"></span>**\_ \_ connessione crittografata WBEM E \_ \_ necessaria**
</dt> <dd> <dl> <dt>

2147750023 (0x80041087)
</dt> <dt>



L'utente ha tentato di impostare un nome computer o un dominio senza una connessione crittografata.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_TIMED_OUT"></span><span id="wbem_e_provider_timed_out"></span>**\_timeout del \_ provider WBEM E \_ \_**
</dt> <dd> <dl> <dt>

2147750024 (0x80041088)
</dt> <dt>



Un provider non è riuscito a segnalare i risultati entro il timeout specificato.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NO_KEY"></span><span id="wbem_e_no_key"></span>**WBEM \_ E \_ Nessuna \_ chiave**
</dt> <dd> <dl> <dt>

2147750025 (0x80041089)
</dt> <dt>



L'utente ha tentato di inserire un'istanza senza chiave definita.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_DISABLED"></span><span id="wbem_e_provider_disabled"></span>**\_provider WBEM \_ E \_ disabilitato**
</dt> <dd> <dl> <dt>

2147750026 (0x8004108A)
</dt> <dt>



L'utente ha tentato di registrare un'istanza del provider ma il server COM per l'istanza del provider è stato scaricato.


</dt> </dl> </dd> <dt>

<span id="WBEMESS_E_REGISTRATION_TOO_BROAD"></span><span id="wbemess_e_registration_too_broad"></span>**registrazione di WBEMESS \_ E \_ \_ troppo \_ ampia**
</dt> <dd> <dl> <dt>

2147753985 (0x80042001)
</dt> <dt>



La registrazione del provider si sovrappone al dominio dell'evento di sistema.


</dt> </dl> </dd> <dt>

<span id="WBEMESS_E_REGISTRATION_TOO_PRECISE"></span><span id="wbemess_e_registration_too_precise"></span>**registrazione di WBEMESS \_ E \_ \_ troppo \_ precisa**
</dt> <dd> <dl> <dt>

2147753986 (0x80042002)
</dt> <dt>



Nella query non è stata utilizzata una clausola WITHIN.


</dt> </dl> </dd> <dt>

<span id="WBEMESS_E_AUTHZ_NOT_PRIVILEGED"></span><span id="wbemess_e_authz_not_privileged"></span>**WBEMESS \_ E \_ AUTHZ \_ senza \_ privilegi**
</dt> <dd> <dl> <dt>

2147753987 (0x80042003)
</dt> <dt>



Il computer non dispone delle autorizzazioni necessarie per il dominio per supportare le funzioni di sicurezza correlate all'istanza di sottoscrizione creata. Contattare l'amministratore di dominio per aggiungere il computer al gruppo di accesso di autorizzazione Windows.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_RETRY_LATER"></span><span id="wbem_e_retry_later"></span>**WBEM \_ E \_ Riprova \_ più tardi**
</dt> <dd> <dl> <dt>

2147758081 (0x80043001)
</dt> <dt>



Riservato per utilizzi futuri.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_RESOURCE_CONTENTION"></span><span id="wbem_e_resource_contention"></span>**\_ \_ contesa di risorse E di WBEM \_**
</dt> <dd> <dl> <dt>

2147758082 (0x80043002)
</dt> <dt>



Riservato per utilizzi futuri.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_QUALIFIER_NAME"></span><span id="wbemmof_e_expected_qualifier_name"></span>**WBEMMOF \_ E \_ \_ Nome qualificatore previsto \_**
</dt> <dd> <dl> <dt>

2147762177 (0x80044001)
</dt> <dt>



Previsto un nome di qualificatore.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_SEMI"></span><span id="wbemmof_e_expected_semi"></span>**WBEMMOF \_ E \_ previsto \_ semi**
</dt> <dd> <dl> <dt>

2147762178 (0x80044002)
</dt> <dt>



Previsto punto e virgola o ' ='.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_OPEN_BRACE"></span><span id="wbemmof_e_expected_open_brace"></span>**WBEMMOF \_ E \_ \_ parentesi graffa di apertura prevista \_**
</dt> <dd> <dl> <dt>

2147762179 (0x80044003)
</dt> <dt>



Prevista parentesi graffa di apertura.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_CLOSE_BRACE"></span><span id="wbemmof_e_expected_close_brace"></span>**WBEMMOF \_ E \_ \_ parentesi graffa di chiusura prevista \_**
</dt> <dd> <dl> <dt>

2147762180 (0x80044004)
</dt> <dt>



Parentesi graffa di chiusura mancante o elemento di matrice non valido.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_CLOSE_BRACKET"></span><span id="wbemmof_e_expected_close_bracket"></span>**WBEMMOF \_ E \_ \_ parentesi chiusa \_ prevista**
</dt> <dd> <dl> <dt>

2147762181 (0x80044005)
</dt> <dt>



È prevista una parentesi di chiusura.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_CLOSE_PAREN"></span><span id="wbemmof_e_expected_close_paren"></span>**WBEMMOF \_ E \_ \_ parentesi chiuse \_ previste**
</dt> <dd> <dl> <dt>

2147762182 (0x80044006)
</dt> <dt>



Prevista parentesi di chiusura.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_ILLEGAL_CONSTANT_VALUE"></span><span id="wbemmof_e_illegal_constant_value"></span>**WBEMMOF \_ E \_ \_ valore costante non valido \_**
</dt> <dd> <dl> <dt>

2147762183 (0x80044007)
</dt> <dt>



Valore numerico non compreso nell'intervallo o nelle stringhe senza virgolette.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_TYPE_IDENTIFIER"></span><span id="wbemmof_e_expected_type_identifier"></span>**WBEMMOF \_ E \_ \_ identificatore di tipo previsto \_**
</dt> <dd> <dl> <dt>

2147762184 (0x80044008)
</dt> <dt>



È previsto un identificatore di tipo.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_OPEN_PAREN"></span><span id="wbemmof_e_expected_open_paren"></span>**WBEMMOF \_ E \_ \_ parentesi aperta \_ prevista**
</dt> <dd> <dl> <dt>

2147762185 (0x80044009)
</dt> <dt>



È prevista una parentesi aperta.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNRECOGNIZED_TOKEN"></span><span id="wbemmof_e_unrecognized_token"></span>**WBEMMOF \_ E \_ token non riconosciuto \_**
</dt> <dd> <dl> <dt>

2147762186 (0x8004400A)
</dt> <dt>



Token imprevisto nel file.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNRECOGNIZED_TYPE"></span><span id="wbemmof_e_unrecognized_type"></span>**WBEMMOF \_ E \_ tipo non riconosciuto \_**
</dt> <dd> <dl> <dt>

2147762187 (0x8004400B)
</dt> <dt>



Identificatore di tipo non riconosciuto o non supportato.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_PROPERTY_NAME"></span><span id="wbemmof_e_expected_property_name"></span>**WBEMMOF \_ E \_ \_ nome della proprietà prevista \_**
</dt> <dd> <dl> <dt>

2147762187 (0x8004400B)
</dt> <dt>



Nome del metodo o della proprietà previsto.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_TYPEDEF_NOT_SUPPORTED"></span><span id="wbemmof_e_typedef_not_supported"></span>**WBEMMOF \_ E \_ typedef \_ non \_ supportati**
</dt> <dd> <dl> <dt>

2147762189 (0x8004400D)
</dt> <dt>



I typedef e i tipi enumerati non sono supportati.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNEXPECTED_ALIAS"></span><span id="wbemmof_e_unexpected_alias"></span>**WBEMMOF \_ E \_ alias imprevisto \_**
</dt> <dd> <dl> <dt>

2147762190 (0x8004400E)
</dt> <dt>



Solo un riferimento a un oggetto classe può avere un valore alias.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNEXPECTED_ARRAY_INIT"></span><span id="wbemmof_e_unexpected_array_init"></span>**WBEMMOF \_ E \_ \_ inizializzazione di matrice imprevista \_**
</dt> <dd> <dl> <dt>

2147762191 (0x8004400F)
</dt> <dt>



Inizializzazione di matrice imprevista. Le matrici devono essere dichiarate con \[ \] .


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_AMENDMENT_SYNTAX"></span><span id="wbemmof_e_invalid_amendment_syntax"></span>**WBEMMOF \_ E \_ \_ sintassi di modifica non valida \_**
</dt> <dd> <dl> <dt>

2147762192 (0x80044010)
</dt> <dt>



Sintassi del percorso dello spazio dei nomi non valida.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_DUPLICATE_AMENDMENT"></span><span id="wbemmof_e_invalid_duplicate_amendment"></span>**WBEMMOF \_ E \_ \_ modifica duplicata non valida \_**
</dt> <dd> <dl> <dt>

2147762193 (0x80044011)
</dt> <dt>



Identificatori di modifica duplicati.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_PRAGMA"></span><span id="wbemmof_e_invalid_pragma"></span>**\_pragma WBEMMOF E \_ non valido \_**
</dt> <dd> <dl> <dt>

2147762194 (0x80044012)
</dt> <dt>



il [ \# pragma](pragma-namespace.md) deve essere seguito da una parola chiave valida.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_NAMESPACE_SYNTAX"></span><span id="wbemmof_e_invalid_namespace_syntax"></span>**WBEMMOF \_ E \_ \_ sintassi dello spazio dei nomi non valida \_**
</dt> <dd> <dl> <dt>

2147762195 (0x80044013)
</dt> <dt>



Sintassi del percorso dello spazio dei nomi non valida.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_CLASS_NAME"></span><span id="wbemmof_e_expected_class_name"></span>**WBEMMOF \_ E \_ il \_ nome della classe previsto \_**
</dt> <dd> <dl> <dt>

2147762196 (0x80044014)
</dt> <dt>



Il carattere imprevisto nel nome della classe deve essere un identificatore.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_TYPE_MISMATCH"></span><span id="wbemmof_e_type_mismatch"></span>**tipo di WBEMMOF \_ E non \_ \_ corrispondente**
</dt> <dd> <dl> <dt>

2147762197 (0x80044015)
</dt> <dt>



Il valore specificato non può essere creato nel tipo appropriato.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_ALIAS_NAME"></span><span id="wbemmof_e_expected_alias_name"></span>**WBEMMOF \_ E \_ \_ nome alias \_ previsto**
</dt> <dd> <dl> <dt>

2147762198 (0x80044016)
</dt> <dt>



Il segno di dollaro deve essere seguito da un nome di alias come identificatore.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_CLASS_DECLARATION"></span><span id="wbemmof_e_invalid_class_declaration"></span>**WBEMMOF \_ E \_ \_ dichiarazione di classe non valida \_**
</dt> <dd> <dl> <dt>

2147762199 (0x80044017)
</dt> <dt>



Dichiarazione di classe non valida.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_INSTANCE_DECLARATION"></span><span id="wbemmof_e_invalid_instance_declaration"></span>**WBEMMOF \_ E \_ \_ dichiarazione di istanza non valida \_**
</dt> <dd> <dl> <dt>

2147762200 (0x80044018)
</dt> <dt>



La dichiarazione dell'istanza non è valida. Deve iniziare con "instance of"


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_DOLLAR"></span><span id="wbemmof_e_expected_dollar"></span>**WBEMMOF \_ E \_ \_ dollaro previsto**
</dt> <dd> <dl> <dt>

2147762201 (0x80044019)
</dt> <dt>



È previsto un segno di dollaro. Un alias nel formato "$name" deve seguire la parola chiave "As".


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_CIMTYPE_QUALIFIER"></span><span id="wbemmof_e_cimtype_qualifier"></span>**\_ \_ qualificatore WBEMMOF E CimType \_**
</dt> <dd> <dl> <dt>

2147762202 (0x8004401A)
</dt> <dt>



Impossibile specificare il qualificatore "CIMTYPE" direttamente in un file MOF. Usare la notazione di tipo standard.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_DUPLICATE_PROPERTY"></span><span id="wbemmof_e_duplicate_property"></span>**WBEMMOF \_ E \_ Proprietà duplicata \_**
</dt> <dd> <dl> <dt>

2147762203 (0x8004401B)
</dt> <dt>



Il nome di proprietà duplicato è stato trovato nel file MOF.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_NAMESPACE_SPECIFICATION"></span><span id="wbemmof_e_invalid_namespace_specification"></span>**WBEMMOF \_ E \_ \_ specifica dello spazio dei nomi non valida \_**
</dt> <dd> <dl> <dt>

2147762204 (0x8004401C)
</dt> <dt>



La sintassi dello spazio dei nomi non è valida. Non sono consentiti riferimenti ad altri server.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_OUT_OF_RANGE"></span><span id="wbemmof_e_out_of_range"></span>**WBEMMOF \_ E \_ non \_ \_ compreso nell'intervallo**
</dt> <dd> <dl> <dt>

2147762205 (0x8004401D)
</dt> <dt>



Il valore non è compreso nell'intervallo.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_FILE"></span><span id="wbemmof_e_invalid_file"></span>**\_file WBEMMOF E \_ non valido \_**
</dt> <dd> <dl> <dt>

2147762206 (0x8004401E)
</dt> <dt>



Il file non è un file MOF di testo o un file MOF binario valido.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_ALIASES_IN_EMBEDDED"></span><span id="wbemmof_e_aliases_in_embedded"></span>**WBEMMOF \_ E \_ alias \_ in \_ Embedded**
</dt> <dd> <dl> <dt>

2147762207 (0x8004401F)
</dt> <dt>



Gli oggetti incorporati non possono essere alias.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_NULL_ARRAY_ELEM"></span><span id="wbemmof_e_null_array_elem"></span>**\_elem WBEMMOF E \_ null \_ array \_**
</dt> <dd> <dl> <dt>

2147762208 (0x80044020)
</dt> <dt>



Gli elementi NULL in una matrice non sono supportati.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_DUPLICATE_QUALIFIER"></span><span id="wbemmof_e_duplicate_qualifier"></span>**WBEMMOF \_ E \_ \_ qualificatore duplicato**
</dt> <dd> <dl> <dt>

2147762209 (0x80044021)
</dt> <dt>



Il qualificatore è stato usato più di una volta per l'oggetto.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_FLAVOR_TYPE"></span><span id="wbemmof_e_expected_flavor_type"></span>**WBEMMOF \_ E \_ \_ tipo di sapore previsto \_**
</dt> <dd> <dl> <dt>

2147762210 (0x80044022)
</dt> <dt>



È previsto un tipo di sapore, ad esempio **ToInstance**, **ToClass**, **EnableOverride** o **DisableOverride**.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES"></span><span id="wbemmof_e_incompatible_flavor_types"></span>**\_tipi di \_ sapore incompatibili con WBEMMOF E \_ \_**
</dt> <dd> <dl> <dt>

2147762211 (0x80044023)
</dt> <dt>



La combinazione di **EnableOverride** e **DisableOverride** nello stesso qualificatore non è valida.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_MULTIPLE_ALIASES"></span><span id="wbemmof_e_multiple_aliases"></span>**WBEMMOF \_ E \_ più \_ alias**
</dt> <dd> <dl> <dt>

2147762212 (0x80044024)
</dt> <dt>



Non è possibile usare due volte un alias.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES2"></span><span id="wbemmof_e_incompatible_flavor_types2"></span>**WBEMMOF \_ E \_ \_ TYPES2 Flavor incompatibili \_**
</dt> <dd> <dl> <dt>

2147762213 (0x80044025)
</dt> <dt>



La **combinazione di** **Restricted** e **ToClass o ToClass** non è valida.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_NO_ARRAYS_RETURNED"></span><span id="wbemmof_e_no_arrays_returned"></span>**WBEMMOF \_ E \_ non sono state \_ \_ restituite matrici**
</dt> <dd> <dl> <dt>

2147762214 (0x80044026)
</dt> <dt>



I metodi non possono restituire valori di matrice.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_MUST_BE_IN_OR_OUT"></span><span id="wbemmof_e_must_be_in_or_out"></span>**WBEMMOF \_ e \_ deve \_ essere \_ in \_ \_ uscita**
</dt> <dd> <dl> <dt>

2147762215 (0x80044027)
</dt> <dt>



Gli argomenti devono avere un qualificatore **in** o **out** .


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_FLAGS_SYNTAX"></span><span id="wbemmof_e_invalid_flags_syntax"></span>**\_sintassi WBEMMOF \_ E \_ flag non validi \_**
</dt> <dd> <dl> <dt>

2147762216 (0x80044028)
</dt> <dt>



Sintassi di flag non valida.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_BRACE_OR_BAD_TYPE"></span><span id="wbemmof_e_expected_brace_or_bad_type"></span>**WBEMMOF \_ e \_ \_ tipo di parentesi graffa prevista \_ o non \_ valido \_**
</dt> <dd> <dl> <dt>

2147762217 (0x80044029)
</dt> <dt>



Manca la parentesi graffa finale e il punto e virgola di una classe.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNSUPPORTED_CIMV22_QUAL_VALUE"></span><span id="wbemmof_e_unsupported_cimv22_qual_value"></span>**WBEMMOF \_ E non \_ supportato \_ CIMV22 \_ qual \_ value**
</dt> <dd> <dl> <dt>

2147762218 (0x8004402A)
</dt> <dt>



Una funzionalità CIM versione 2,2 non è supportata per un valore qualificatore.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNSUPPORTED_CIMV22_DATA_TYPE"></span><span id="wbemmof_e_unsupported_cimv22_data_type"></span>**WBEMMOF \_ E \_ \_ tipo di dati CIMV22 \_ non \_ supportato**
</dt> <dd> <dl> <dt>

2147762219 (0x8004402B)
</dt> <dt>



Il tipo di dati CIM versione 2,2 non è supportato.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_DELETEINSTANCE_SYNTAX"></span><span id="wbemmof_e_invalid_deleteinstance_syntax"></span>**WBEMMOF \_ E \_ \_ sintassi DELETEINSTANCE non valida \_**
</dt> <dd> <dl> <dt>

2147762220 (0x8004402C)
</dt> <dt>



La sintassi dell'istanza Delete non è valida. Dovrebbe essere `#pragma DeleteInstance("instancepath", FAIL|NOFAIL)`


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_QUALIFIER_SYNTAX"></span><span id="wbemmof_e_invalid_qualifier_syntax"></span>**WBEMMOF \_ E \_ \_ sintassi di qualificatore non valida \_**
</dt> <dd> <dl> <dt>

2147762221 (0x8004402D)
</dt> <dt>



Sintassi del qualificatore non valida. Il valore dovrebbe essere `qualifiername:type=value,scope(class|instance), flavorname`.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_QUALIFIER_USED_OUTSIDE_SCOPE"></span><span id="wbemmof_e_qualifier_used_outside_scope"></span>**\_ \_ qualificatore WBEMMOF E \_ usato \_ all'esterno dell' \_ ambito**
</dt> <dd> <dl> <dt>

2147762222 (0x8004402E)
</dt> <dt>



Il qualificatore viene usato al di fuori dell'ambito.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_ERROR_CREATING_TEMP_FILE"></span><span id="wbemmof_e_error_creating_temp_file"></span>**WBEMMOF \_ E \_ errore durante la \_ creazione del \_ \_ file temporaneo**
</dt> <dd> <dl> <dt>

2147762223 (0x8004402F)
</dt> <dt>



Errore durante la creazione del file temporaneo. Il file temporaneo è una fase intermedia della compilazione MOF.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_ERROR_INVALID_INCLUDE_FILE"></span><span id="wbemmof_e_error_invalid_include_file"></span>**\_errore WBEMMOF \_ E \_ \_ file di inclusione non valido \_**
</dt> <dd> <dl> <dt>

2147762224 (0x80044030)
</dt> <dt>



Un file incluso nel file MOF tramite il comando per il preprocessore [ \# include](-include.md) non è valido.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_DELETECLASS_SYNTAX"></span><span id="wbemmof_e_invalid_deleteclass_syntax"></span>**WBEMMOF \_ E \_ \_ sintassi DELETECLASS non valida \_**
</dt> <dd> <dl> <dt>

2147762225 (0x80044031)
</dt> <dt>



La sintassi per i comandi del preprocessore [ \# pragma DeleteInstance](pragma-deleteinstance.md) o [ \# pragma deleteclass](pragma-deleteclass.md) non è valida.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Intestazione<br/>                   | <dl> <dt>WbemCli. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WbemCli. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici restituiti WMI](wmi-return-codes.md)
</dt> </dl>

 

