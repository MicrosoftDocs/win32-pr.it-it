---
description: Dopo aver recuperato le informazioni di installazione da un file INF, sono disponibili diverse funzioni di gestione dei file che è possibile usare per installare i file elencati in una sezione INF.
ms.assetid: 4e6042a0-36a9-4f74-b6cc-554e7f7aa2d9
title: Installazione da un file INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e32780855e126eaaa38ae937a265951711662434e90ab0ffb425e2e4f4f6c42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867571"
---
# <a name="installing-from-an-inf-file"></a>Installazione da un file INF

Dopo aver recuperato le informazioni di installazione da un file INF, sono disponibili diverse funzioni di gestione dei file che è possibile usare per installare i file elencati in una sezione INF. Le funzioni di basso livello, ad [**esempio SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea) e [**SetupInstallFileEx,**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa) installano un singolo file.

Sono disponibili anche funzioni per gestire i file compressi. La [**funzione SetupGetFileCompressionInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfilecompressioninfoa) restituisce informazioni sui file compressi. Queste informazioni possono quindi essere usate da [**SetupDecompressOrCopyFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupdecompressorcopyfilea) per copiare e, se necessario, espandere il file.

Funzioni di alto livello come [**SetupInstallFromInfSection,**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona)e [**SetupInstallServicesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallservicesfrominfsectiona) elaborano le operazioni di installazione in una sezione **Install** **o Service.** Di questi, **SetupInstallFromInfSection** è il più versatile perché può eseguire qualsiasi tipo di operazione di installazione elencata nella **sezione Install** di un file INF. Sono incluse le operazioni del Registro di sistema e INI elencate nelle righe **AddReg**, **DelReg**, **UpdateInis** o **UpdateIniField** di una **sezione Install.**

Le funzioni [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona) e [**SetupInstallServicesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallservicesfrominfsectiona) accodano le operazioni rispettivamente da una sezione **Install** o **Service** a una coda di file esistente. Si noti che è necessario chiamare SetupInstallFromInfSection e SetupInstallServicesFromInfSection separatamente per le operazioni e i servizi della coda. Per altre informazioni, vedere [Code di file.](file-queues.md)

Al contrario, la [**funzione SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) crea ed elimina la propria coda interna. Un uso comune di **SetupInstallFromInfSection** è chiamarlo dopo che tutti i file sono stati copiati correttamente per eseguire il Registro di sistema e le transazioni INI.

In Windows 2000 i file DLL possono essere autoregistrati chiamando [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) in un file INF che include la direttiva **RegisterDlls** nella relativa sezione **Install.** **SetupInstallFromInfSection** può anche eseguire la registrazione automatica di DLL a 32 bit da un processo a 64 bit.

Nei sistemi operativi a 64 bit è possibile chiamare [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) per eseguire operazioni sulla parte a 32 bit del Registro di sistema. Per aggiungere una chiave del Registro di sistema alla parte a 32 bit del Registro di sistema, includere il \_ flag FLG ADDREG \_ 32BITKEY nella riga **AddReg** del file INF. Per eliminare una chiave del Registro di sistema solo nella parte a 32 bit del Registro di sistema, includere la chiave FLG \_ DELREG \_ 32BITKEY nella **riga DelReg.** Per impostare o cancellare un valore binario solo nella parte a 32 bit del Registro di sistema, includere FLG \_ BITREG \_ 32BITKEY nella **riga BitReg.**

Oltre alle funzioni elencate in precedenza, l'API di installazione include funzioni che accodano le operazioni di installazione dei file, per file o per sezione INF. Per altre informazioni, vedere [Code di file.](file-queues.md)

 

 



