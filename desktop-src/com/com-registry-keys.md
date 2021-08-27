---
title: Chiavi del Registro di sistema COM
description: Chiavi del Registro di sistema COM
ms.assetid: 08406092-eb77-4001-a4fa-659ce945e4d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80800bda0123823fec85a514c19031d485b17baca729969b4e74e5f08516eecd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048499"
---
# <a name="com-registry-keys"></a>Chiavi del Registro di sistema COM

Il Registro di sistema contiene una grande quantità di informazioni usate da COM. Le informazioni più importanti vengono archiviate nelle chiavi seguenti.



| Chiave                                                                 | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AppID](appid-key.md)<br/>                                   | Raggruppa le opzioni di configurazione (un set di valori denominati) per uno o più oggetti COM distribuiti in un'unica posizione nel Registro di sistema. Le sottochiavi in questa chiave vengono usate per eseguire il mapping di un identificatore di applicazione (AppID) a un nome di server remoto. Per semplificare la gestione delle impostazioni comuni di sicurezza e configurazione, gli oggetti COM distribuiti ospitati dallo stesso eseguibile vengono raggruppati in un unico AppID.<br/>                                                                                                                                                                                                                                                                                                                      |
| [Clsid](clsid-key-hklm.md)<br/>                              | Un identificatore di classe (CLSID) è un identificatore univoco globale che identifica un oggetto classe COM. Se il server o il contenitore consente il collegamento a oggetti incorporati, registrare un CLSID per ogni classe di oggetti supportata. La chiave CLSID contiene informazioni utilizzate dal gestore COM predefinito per restituire informazioni su una classe quando è in esecuzione.<br/> Per ottenere un CLSID per l'applicazione, usare uuidgen.exe, disponibile nella directory TOOLs del Toolkit COM, oppure \\ [**usare CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid). <br/>                                                                                                                                                                                       |
| [ProgID](-progid--key.md)<br/>                               | Un identificatore programmatico (ProgID) è una voce del Registro di sistema che può essere associata a un CLSID. Il tasto ProgID esegue il mapping di una stringa descrittiva a un CLSID. Come il CLSID, il ProgID identifica una classe, ma con una precisione minore. Usare un ProgID nelle situazioni di programmazione in cui non è possibile usare un CLSID. I ProgID non devono essere visualizzati nell'interfaccia utente. Non è garantito che i ProgID siano univoci, quindi possono essere usati solo quando non si verificano conflitti di nome.<br/>                                                                                                                                                                                                                                                      |
| [VersionIndependentProgID](versionindependentprogid.md)<br/> | Associa un ProgID a un CLSID. Viene usato per determinare la versione più recente di un'applicazione oggetto. Come il ProgID, il ProgID indipendente dalla versione può essere registrato con un nome leggibile. <br/> Le applicazioni devono registrare un identificatore a livello di codice indipendente dalla versione nella chiave VersionIndependentProgID. Il ProgID indipendente dalla versione fa riferimento alla classe dell'applicazione e non cambia da una versione all'altra, ma rimane costante in tutte le versioni. Viene usato con i linguaggi macro e fa riferimento alla versione attualmente installata della classe dell'applicazione. Il ProgID indipendente dalla versione deve corrispondere al nome della versione più recente dell'applicazione dell'oggetto. <br/> |
| [estensione \_ di file](-file-extension--key.md)<br/>              | Associa un'estensione di file a un ProgID.<br/> Le informazioni contenute nella chiave di estensione del nome file vengono usate sia dal moniker di sistema che [dai moniker di file](file-monikers.md). [**GetClassFile usa**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) la chiave di estensione del nome file per fornire il CLSID associato. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Interfaccia](interface-key.md)<br/>                           | Registra le nuove interfacce associando un nome di interfaccia a un identificatore di interfaccia (IID). Esegue il mapping degli IID a informazioni specifiche di un'interfaccia. Le informazioni sono necessarie principalmente per l'uso di interfacce oltre i limiti del processo. <br/> Quando si aggiunge una nuova interfaccia, è necessario completare la chiave interface perché COM registri la nuova interfaccia. Deve essere presente una sottochiave IID per ogni nuova interfaccia. <br/>                                                                                                                                                                                                                                                                                                       |
| [Ole](hkey-local-machine-software-microsoft-ole.md)<br/>     | Controlla le autorizzazioni di avvio e accesso predefinite per gli oggetti COM distribuiti, nonché le funzionalità di sicurezza a livello di chiamata per le applicazioni che non chiamano [**CoInitializeSecurity.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) Solo gli amministratori hanno accesso completo a questa parte del Registro di sistema. Tutti gli altri utenti hanno accesso in sola lettura. <br/>                                                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione di applicazioni COM](registering-com-applications.md)
</dt> </dl>

 

 





