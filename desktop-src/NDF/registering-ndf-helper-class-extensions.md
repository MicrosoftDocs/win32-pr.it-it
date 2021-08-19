---
title: Registrazione delle estensioni della classe helper NDF
description: A ogni estensione di classe helper sono associate diverse chiavi del Registro di sistema. Alcune chiavi sono richieste da COM e alcune chiavi sono richieste da NDF.
ms.assetid: 9ff3266d-5ffc-4a00-be24-2f85461c6ea6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6457e144abdeb1dbed1e33bb10e21302f918da8cdc5a6fd2090f3665e83f0316
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117798498"
---
# <a name="registering-ndf-helper-class-extensions"></a>Registrazione delle estensioni della classe helper NDF

A ogni estensione di classe helper sono associate diverse chiavi del Registro di sistema. Alcune chiavi sono richieste da COM e alcune chiavi sono richieste da NDF.

## <a name="com-registry-keys"></a>Chiavi del Registro di sistema COM

Le estensioni della classe helper devono essere implementate come server COM. La registrazione COM deve essere completata per ogni estensione della classe helper. È necessario registrare il CLSID dell'oggetto, [**l'interfaccia INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo) e [**l'interfaccia INetDiagHelper.**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) La registrazione crea una serie di chiavi del Registro di sistema correlate a COM per l'estensione della classe helper NDF.

## <a name="ndf-registry-keys"></a>Chiavi del Registro di sistema NDF

Le estensioni della classe helper devono essere registrate prima di interagire con Framework di diagnostica di rete e con altre classi helper correlate. Questa operazione viene eseguita popolando il Registro di sistema.

La procedura seguente illustra come aggiungere estensioni di classe helper al Registro di sistema.

1.  Pubblicare i nomi delle classi helper implementate dalla DLL e le relative dipendenze creando una chiave per la DLL in

    **HKLM \\ System \\ CurrentControlSet \\ Control \\ NetDiagFx** \\ *VendorName* \\ **HostDLLs** \\ *Helper Class DLL* \\ **HelperClasses** Helper Class \\ *Name*

    Sostituire *VendorName,* *Helper Class DLL* e Helper Class *Name* con valori definiti dall'utente come descritto di seguito.

    | Valore               | Type    | Significato                                                                      |
    |---------------------|---------|------------------------------------------------------------------------------|
    | *VendorName*        | REG \_ SZ | Nome del fornitore.                                                      |
    | *DLL della classe helper*  | REG \_ SZ | Nome della DLL, senza estensione.                                          |
    | *Nome classe helper* | REG \_ SZ | Nome della classe helper da cui dipende la classe helper corrente. |

    

     

2.  In ogni *chiave nome classe helper* pubblicare le informazioni seguenti.

    

    | Valore         | Type       | Significato                                                                                                                                                                 |
    |---------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **Clsid**     | REG \_ SZ    | Stringa che contiene l'ID classe COM della classe helper.                                                                                                            |
    | **Version**   | REG \_ SZ    | Stringa contenente le versioni principale e secondaria della classe helper nel formato <major> <minor> .                                                        |
    | **Pubblicato** | REG \_ DWORD | Il valore 1 indica che questa classe helper deve essere richiamata direttamente dal client di diagnostica. 0 indica che può essere chiamato solo da un'altra classe helper. |
    | **Parent**    | REG \_ SZ    | Stringa che indica il nome della classe helper estendibile Microsoft da estendere.                                                                                       |

    

     

3.  Per ogni classe helper, pubblicare l'elenco di attributi corrispondenti creando una chiave in

    **HKLM \\ Controllo \\ System CurrentControlSet \\ \\ NetDiagFx** \\ *VendorName* \\ **HostDLLs** Classe \\ *helper DLL* \\ **HelperClasses Nome** classe \\ *helper* \\ **MatchAttributes**

    La chiave deve contenere uno o più valori (uno per attributo) del tipo seguente.

    | Valore             | Type                             | Significato                                                                    |
    |-------------------|----------------------------------|----------------------------------------------------------------------------|
    | **AttributeName** | REG \_ SZ \| REG \_ DWORD \| REG \_ BINARY | Valore che completa la coppia nome/valore per un attributo specifico. |

    

     

 

 




