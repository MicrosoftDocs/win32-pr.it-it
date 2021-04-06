---
description: Una volta recuperate le informazioni di installazione da un file INF, sono disponibili diverse funzioni di gestione dei file che è possibile utilizzare per installare i file elencati in una sezione INF.
ms.assetid: 4e6042a0-36a9-4f74-b6cc-554e7f7aa2d9
title: Installazione da un file INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bc3642edfb7abc2864c2c0784c79fbb21612fb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883581"
---
# <a name="installing-from-an-inf-file"></a>Installazione da un file INF

Una volta recuperate le informazioni di installazione da un file INF, sono disponibili diverse funzioni di gestione dei file che è possibile utilizzare per installare i file elencati in una sezione INF. Le funzioni di basso livello, ad esempio [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea) e [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa) , installano un singolo file.

Sono inoltre disponibili funzioni per la gestione dei file compressi. La funzione [**SetupGetFileCompressionInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfilecompressioninfoa) restituisce informazioni sui file compressi. Queste informazioni possono quindi essere usate da [**SetupDecompressOrCopyFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupdecompressorcopyfilea) per copiare e, se necessario, espandere il file.

Funzioni di alto livello, ad esempio [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona), [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona)e [**SetupInstallServicesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallservicesfrominfsectiona) , elaborano le operazioni di installazione in una sezione **relativa all'installazione o al** **servizio** . Di questi, **SetupInstallFromInfSection** è la più versatile perché può eseguire qualsiasi tipo di operazione di installazione elencata nella sezione **Install** di un file inf. Sono incluse le operazioni del registro di sistema e INI elencate nelle righe **AddReg**, **DelReg**, **UpdateInis** o **UpdateIniField** di una sezione di **installazione** .

Le funzioni [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona) e [**SetupInstallServicesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallservicesfrominfsectiona) accodano rispettivamente le operazioni da una sezione **Install** o **Service** a una coda di file esistente. Si noti che è necessario chiamare SetupInstallFromInfSection e SetupInstallServicesFromInfSection separatamente per accodare operazioni e servizi. Per altre informazioni, vedere [code di file](file-queues.md).

Al contrario, la funzione [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) crea ed Elimina definitivamente la propria coda interna. Un uso comune di **SetupInstallFromInfSection** consiste nel chiamarlo dopo che tutti i file sono stati copiati correttamente per eseguire il registro di sistema e le transazioni ini.

In Windows 2000, i file DLL possono essere registrati autonomamente chiamando [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) in un file inf che include la direttiva **RegisterDlls** nella relativa sezione di **installazione** . **SetupInstallFromInfSection** è anche in grado di registrare autonomamente dll a 32 bit da un processo a 64 bit.

Nei sistemi operativi a 64 bit, è possibile chiamare [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) per eseguire operazioni sulla parte del registro di sistema a 32 bit. Per aggiungere una chiave del registro di sistema alla parte 32 bit del registro di sistema, includere \_ il \_ flag FLG ADDREG 32BITKEY nella riga **ADDREG** del codice INF. Per eliminare una chiave del registro di sistema solo nella parte a 32 bit del registro di sistema, includere la \_ chiave 32BITKEY di FLG DELREG \_ nella riga **DELREG** . Per impostare o deselezionare un valore binario solo nella parte a 32 bit del registro di sistema, includere il \_ 32BITKEY FLG BITREG \_ nella riga **BITREG** .

Oltre alle funzioni elencate in precedenza, l'API di installazione include funzioni che accodano le operazioni di installazione dei file, per file o per sezione INF. Per altre informazioni, vedere [code di file](file-queues.md).

 

 



