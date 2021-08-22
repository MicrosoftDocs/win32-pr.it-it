---
description: 'Altre informazioni su: Esempio di servizio completo'
ms.assetid: a3aeea9b-09c0-4834-892a-c378b67402f4
title: Esempio di servizio completo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1f3f5fc0fb59342841a9d1f1280475ace12c54998d59e5f36a19557f0ccc5c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888332"
---
# <a name="the-complete-service-sample"></a>Esempio di servizio completo

Gli argomenti di questa sezione formano un esempio di servizio completo:

-   [Sample.mc](sample-mc.md) (contiene messaggi di errore)
-   [Svc.cpp](svc-cpp.md) (contiene il codice del servizio)
-   [SvcConfig.cpp (contiene](svcconfig-cpp.md) il codice di configurazione del servizio)
-   [SvcControl.cpp (contiene](svccontrol-cpp.md) il codice di controllo del servizio)

## <a name="building-the-service"></a>Compilazione del servizio

La procedura seguente descrive come compilare il servizio e registrare la DLL del messaggio di evento.

**Per compilare il servizio e registrare la DLL del messaggio di evento**

1.  Compilare la DLL del messaggio Sample.mc seguendo questa procedura:
    1.  **mc -U sample.mc**
    2.  **rc -r sample.rc**
    3.  **link -dll -noentry -out:sample.dll sample.res**
2.  Compilare Svc.exe, SvcConfig.exe e SvcControl.exe da Svc.cpp, SvcConfig.cpp e SvcControl.cpp, rispettivamente.
3.  Creare la chiave del Registro di sistema **HKEY \_ LOCAL MACHINE SYSTEM \_ \\ \\ CurrentControlSet \\ Services \\ EventLog Application \\ \\ SvcName** e aggiungere i valori del Registro di sistema seguenti a questa chiave.

    | Valore                              | Tipo       | Descrizione                                                                                                        |
    |------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------|
    | **EventMessageFile**  =  *percorso \_ dll* | REG \_ SZ    | Percorso della DLL di sola risorsa che contiene stringhe che il servizio può scrivere nel registro eventi.               |
    | **TypesSupported** = 0x00000007    | REG \_ DWORD | Maschera di bit che specifica i tipi di evento supportati. Il valore 0x000000007 indica che sono supportati tutti i tipi. |

    

     

## <a name="testing-the-service"></a>Test del servizio

La procedura seguente descrive come testare il servizio.

**Per eseguire il test del servizio**

1.  In Pannello di controllo avviare **l'applicazione** Servizi. Nei passaggi seguenti usare il tasto F5 per aggiornare la visualizzazione dopo l'esecuzione di un comando che modifica le informazioni **nell'applicazione** Services.
2.  Eseguire il comando seguente per installare il servizio:

    **svc install**

    Il servizio scrive "Servizio installato correttamente" nella console se l'operazione ha esito positivo o se viene visualizzato un messaggio di errore in caso contrario.

    Se l'installazione del servizio ha esito positivo, il servizio viene visualizzato **nell'applicazione** Servizi. Si noti che **Nome** è impostato su  "SvcName",  Descrizione e Stato sono vuoti e Tipo **di** avvio è impostato su "Manuale".

3.  Eseguire il comando seguente per avviare il servizio:

    **svccontrol start SvcName**

    Se l'operazione ha esito positivo, il programma di controllo del servizio scrive "Avvio servizio in sospeso..." e quindi "Il servizio è stato avviato correttamente" nella console. In caso contrario, il programma scrive un messaggio di errore nella console.

    Se il servizio viene avviato correttamente, **Lo stato** è impostato su "Avviato". Il codice nella [*funzione ServiceMain*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) viene eseguito da Gestione controllo servizi. Se si verifica un errore, il servizio scriverà un messaggio di errore nel registro eventi. Questo messaggio include il nome della funzione che ha avuto esito negativo e il codice di errore restituito in caso di errore.

4.  Eseguire il comando seguente per aggiornare la descrizione del servizio:

    **svcconfig describe SvcName**

    Il programma di configurazione del servizio scrive "Descrizione del servizio aggiornata correttamente" nella console se l'operazione ha esito positivo o viene visualizzato un messaggio di errore in caso contrario.

    Se l'aggiornamento ha esito positivo, **Description** viene impostato su "This is a test description".

5.  Eseguire il comando seguente per eseguire query sulla configurazione del servizio:

    **Query svcconfig SvcName**

    Il programma di configurazione del servizio scrive le informazioni di configurazione del servizio nella console se l'operazione ha esito positivo o se viene visualizzato un messaggio di errore in caso contrario.

6.  Eseguire il comando seguente per modificare l'elenco DACL del servizio:

    **svccontrol dacl SvcName**

    Il programma di configurazione del servizio scrive "Service DACL updated successfully" nella console se l'operazione ha esito positivo o viene visualizzato un messaggio di errore in caso contrario.

7.  Eseguire il comando seguente per disabilitare il servizio:

    **svcconfig disable SvcName**

    Il programma di configurazione del servizio scrive "Servizio disabilitato correttamente" nella console se l'operazione ha esito positivo o viene visualizzato un messaggio di errore in caso contrario.

    Se il servizio viene disabilitato correttamente, **tipo di avvio** è impostato su "Disabilitato".

8.  Eseguire il comando seguente per abilitare il servizio:

    **svcconfig enable SvcName**

    Il programma di configurazione del servizio scrive "Servizio abilitato correttamente" nella console se l'operazione ha esito positivo o viene visualizzato un messaggio di errore in caso contrario.

    Se il servizio è abilitato correttamente, **tipo di avvio** è impostato su "Manuale".

9.  Eseguire il comando seguente per arrestare il servizio:

    **svccontrol stop SvcName**

    Se l'operazione ha esito positivo, il programma di controllo del servizio scrive "Arresto del servizio in sospeso..." e quindi "Il servizio è stato arrestato correttamente" nella console. In caso contrario, il programma scrive un messaggio di errore nella console.

    Se il servizio viene arrestato correttamente, **lo stato** è vuoto.

    Se l'arresto del servizio non riesce, il programma di controllo del servizio scrive un messaggio di errore nel registro eventi che include il nome della funzione non riuscita e il codice di errore restituito in caso di errore.

10. Eseguire il comando seguente per eliminare il servizio:

    **svcconfig delete SvcName**

    Il programma di configurazione del servizio scrive "Servizio eliminato correttamente" nella console se l'operazione ha esito positivo o viene visualizzato un messaggio di errore in caso contrario.

    Se il servizio viene eliminato correttamente, non viene più visualizzato **nell'applicazione** Servizi. Si noti che se si tenta di eliminare un servizio  che non viene arrestato, l'operazione ha esito positivo ma il tipo di avvio è impostato su "Disabilitato" e la voce del servizio verrà eliminata al riavvio del sistema o quando il servizio viene terminato usando Gestione attività.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei servizi](using-services.md)
</dt> </dl>

 

 
