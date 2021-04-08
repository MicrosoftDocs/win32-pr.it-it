---
title: Chiavi del registro di sistema COM
description: Chiavi del registro di sistema COM
ms.assetid: 08406092-eb77-4001-a4fa-659ce945e4d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76b85bb84b0a6f2e6ccc233b68af2889f4cb11ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856245"
---
# <a name="com-registry-keys"></a>Chiavi del registro di sistema COM

Nel registro di sistema sono contenute numerose informazioni utilizzate da COM. Le informazioni più importanti sono archiviate nelle chiavi seguenti.



| Chiave                                                                 | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AppID](appid-key.md)<br/>                                   | Raggruppa le opzioni di configurazione (un set di valori denominati) per uno o più oggetti COM distribuiti in un'unica posizione nel registro di sistema. Le sottochiavi sotto questa chiave vengono usate per eseguire il mapping di un identificatore dell'applicazione (AppID) a un nome di server remoto. Per semplificare la gestione delle impostazioni comuni di sicurezza e configurazione, gli oggetti COM distribuiti ospitati dallo stesso eseguibile vengono raggruppati in un AppID.<br/>                                                                                                                                                                                                                                                                                                                      |
| [CLSID](clsid-key-hklm.md)<br/>                              | Un identificatore di classe (CLSID) è un identificatore univoco globale che identifica un oggetto classe COM. Se il server o il contenitore consente il collegamento a oggetti incorporati, registrare un CLSID per ogni classe di oggetti supportata. La chiave CLSID contiene le informazioni utilizzate dal gestore COM predefinito per restituire informazioni su una classe quando si trova nello stato in esecuzione.<br/> Per ottenere un CLSID per l'applicazione, usare uuidgen.exe, disponibile nella \\ directory degli strumenti di com Toolkit, oppure usare [**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid). <br/>                                                                                                                                                                                       |
| [ProgID](-progid--key.md)<br/>                               | Un identificatore a livello di codice (ProgID) è una voce del registro di sistema che può essere associata a un CLSID. La chiave ProgID esegue il mapping di una stringa intuitiva a un CLSID. Analogamente al CLSID, ProgID identifica una classe, ma con una minore precisione. Usare un ProgID in situazioni di programmazione in cui non è possibile usare un CLSID. I ProgID non devono essere visualizzati nell'interfaccia utente. Non è garantito che i ProgID siano univoci, quindi possono essere usati solo se non si verificano conflitti di nomi.<br/>                                                                                                                                                                                                                                                      |
| [VersionIndependentProgID](versionindependentprogid.md)<br/> | Associa un ProgID a un CLSID. Viene utilizzato per determinare la versione più recente di un'applicazione dell'oggetto. Come il ProgID, il ProgID indipendente dalla versione può essere registrato con un nome leggibile. <br/> Le applicazioni devono registrare un identificatore programmatico indipendente dalla versione sotto la chiave VersionIndependentProgID. Il ProgID indipendente dalla versione fa riferimento alla classe dell'applicazione e non passa da una versione all'altra, rimanendo invece costante in tutte le versioni. Viene usato con i linguaggi macro e si riferisce alla versione attualmente installata della classe dell'applicazione. Il ProgID indipendente dalla versione deve corrispondere al nome della versione più recente dell'applicazione dell'oggetto. <br/> |
| [estensione di file \_](-file-extension--key.md)<br/>              | Associa un'estensione di file a un ProgID.<br/> Le informazioni contenute nella chiave di estensione del nome file vengono utilizzate sia dal moniker di sistema che da quello del [file](file-monikers.md). [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) usa la chiave di estensione del nome file per fornire il CLSID associato. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Interfaccia](interface-key.md)<br/>                           | Registra le nuove interfacce associando il nome di un'interfaccia a un identificatore di interfaccia (IID). Esegue il mapping di IID alle informazioni specifiche di un'interfaccia. Le informazioni sono necessarie principalmente per l'utilizzo di interfacce tra i limiti dei processi. <br/> Quando si aggiunge una nuova interfaccia, è necessario completare la chiave di interfaccia affinché COM registri la nuova interfaccia. Deve essere presente una sottochiave IID per ogni nuova interfaccia. <br/>                                                                                                                                                                                                                                                                                                       |
| [OLE](hkey-local-machine-software-microsoft-ole.md)<br/>     | Controlla le autorizzazioni di avvio e accesso predefinite per gli oggetti COM distribuiti, nonché le funzionalità di sicurezza a livello di chiamata per le applicazioni che non chiamano [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Solo gli amministratori hanno accesso completo a questa parte del registro di sistema. Tutti gli altri utenti hanno accesso in sola lettura. <br/>                                                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione di applicazioni COM](registering-com-applications.md)
</dt> </dl>

 

 





