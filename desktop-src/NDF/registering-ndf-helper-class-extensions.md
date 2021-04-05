---
title: Registrazione delle estensioni di classe helper NDF
description: A ogni estensione della classe helper è associata una serie di chiavi del registro di sistema. Alcune chiavi sono richieste da COM e alcune chiavi sono richieste da NDF.
ms.assetid: 9ff3266d-5ffc-4a00-be24-2f85461c6ea6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f211517a975bdef61db7937fffa95f13beddc156
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714671"
---
# <a name="registering-ndf-helper-class-extensions"></a>Registrazione delle estensioni di classe helper NDF

A ogni estensione della classe helper è associata una serie di chiavi del registro di sistema. Alcune chiavi sono richieste da COM e alcune chiavi sono richieste da NDF.

## <a name="com-registry-keys"></a>Chiavi del registro di sistema COM

Le estensioni della classe helper devono essere implementate come server COM. Per ogni estensione della classe helper è necessario completare la registrazione COM. È necessario registrare il CLSID dell'oggetto, l'interfaccia [**INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo) e l'interfaccia [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) . La registrazione crea una serie di chiavi del registro di sistema correlate a COM per l'estensione della classe helper NDF.

## <a name="ndf-registry-keys"></a>Chiavi del registro di sistema NDF

È necessario registrare le estensioni della classe helper prima di interagire con il Framework di diagnostica di rete e con altre classi helper correlate. Questa operazione viene eseguita popolando il registro di sistema.

Nella procedura seguente viene illustrato come aggiungere estensioni di classe helper al registro di sistema.

1.  Pubblicare i nomi delle classi helper implementate dalla DLL e le relative dipendenze creando una chiave per la DLL in

    **HKLM \\ System \\ CurrentControlSet \\ Control \\ NetDiagFx** \\ *VendorName* \\ **HostDLLs** \\ *Helper Class dll* \\ **HelperClasses** \\ *Helper Class nome classe helper*

    Sostituire *VendorName*, la *dll della classe helper* e il *nome della classe helper* con i valori definiti dall'utente, come descritto di seguito.

    | Valore               | Type    | Significato                                                                      |
    |---------------------|---------|------------------------------------------------------------------------------|
    | *NomeFornitore*        | REG \_ SZ | Nome del fornitore.                                                      |
    | *DLL della classe helper*  | REG \_ SZ | Nome della DLL senza estensione.                                          |
    | *Nome classe helper* | REG \_ SZ | Nome della classe helper da cui dipende la classe helper corrente. |

    

     

2.  In ogni chiave del *nome della classe helper* pubblicare le informazioni seguenti.

    

    | Valore         | Type       | Significato                                                                                                                                                                 |
    |---------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **CLSID**     | REG \_ SZ    | Stringa che contiene l'ID della classe COM della classe helper.                                                                                                            |
    | **Versione**   | REG \_ SZ    | Stringa che contiene le versioni principale e secondaria della classe helper nel formato <major> <minor> .                                                        |
    | **Pubblicato** | REG \_ DWORD | Il valore 1 indica che questa classe helper dovrebbe essere richiamata direttamente dal client di diagnostica. 0 indica che può essere chiamato solo da un'altra classe helper. |
    | **Parent**    | REG \_ SZ    | Stringa che denomina la classe helper Microsoft estendibile che viene estesa.                                                                                       |

    

     

3.  Per ogni classe helper, pubblicare l'elenco degli attributi corrispondenti creando una chiave in

    **HKLM \\ System \\ CurrentControlSet \\ Control \\ NetDiagFx** \\ *VendorName* \\ **HostDLLs** \\ *Helper Class dll* \\ **HelperClasses** \\ *Helper Class nome* \\ **MatchAttributes**

    La chiave deve contenere uno o più valori (uno per ogni attributo) del tipo seguente.

    | Valore             | Type                             | Significato                                                                    |
    |-------------------|----------------------------------|----------------------------------------------------------------------------|
    | **AttributeName** | reg \_ SZ \| reg \_ DWORD \| reg \_ Binary | Valore che completa la coppia di nome e valore per un attributo specifico. |

    

     

 

 




