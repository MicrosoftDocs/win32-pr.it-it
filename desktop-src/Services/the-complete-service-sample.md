---
description: "Altre informazioni su: l'esempio completo del servizio"
ms.assetid: a3aeea9b-09c0-4834-892a-c378b67402f4
title: Esempio di servizio completo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb87ebfef3f964eacee66be94a4b5291c335d0d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316086"
---
# <a name="the-complete-service-sample"></a>Esempio di servizio completo

Gli argomenti di questa sezione costituiscono un esempio di servizio completo:

-   [Sample.MC](sample-mc.md) (contiene messaggi di errore)
-   [Svc. cpp](svc-cpp.md) (contiene il codice del servizio)
-   [SvcConfig. cpp](svcconfig-cpp.md) (contiene il codice di configurazione del servizio)
-   [SvcControl. cpp](svccontrol-cpp.md) (contiene il codice di controllo del servizio)

## <a name="building-the-service"></a>Compilazione del servizio

Nella procedura seguente viene descritto come compilare il servizio e registrare la DLL del messaggio di evento.

**Per compilare il servizio e registrare la DLL del messaggio di evento**

1.  Compilare la DLL del messaggio da Sample.mc attenendosi alla procedura seguente:
    1.  **MC-U sample.mc**
    2.  **esempio RC-r. RC**
    3.  **link-DLL-NOENTRY -out:sample.dll Sample. res**
2.  Compilare rispettivamente Svc.exe, SvcConfig.exe e SvcControl.exe da svc. cpp, SvcConfig. cpp e SvcControl. cpp.
3.  Creare la chiave del registro di **\_ sistema HKEY LOCAL \_ Machine \\ System \\ CurrentControlSet \\ Services \\ EventLog \\ Application \\ SvcName** e aggiungere i valori del registro di sistema seguenti a questa chiave.

    | Valore                              | Tipo       | Descrizione                                                                                                        |
    |------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------|
    | **EventMessageFile**  =  *\_ percorso dll* | REG \_ SZ    | Percorso della DLL di sole risorse contenente le stringhe che il servizio è in grado di scrivere nel log eventi.               |
    | **TypesSupported** = 0x00000007    | REG \_ DWORD | Maschera di bit che specifica i tipi di evento supportati. Il valore 0x000000007 indica che sono supportati tutti i tipi. |

    

     

## <a name="testing-the-service"></a>Test del servizio

Nella procedura seguente viene descritto come eseguire il test del servizio.

**Per eseguire il test del servizio**

1.  Nel pannello di controllo avviare l'applicazione dei **Servizi** . Nei passaggi seguenti usare il tasto F5 per aggiornare la visualizzazione dopo l'esecuzione di un comando che modifica le informazioni nell'applicazione dei **Servizi** .
2.  Eseguire il comando seguente per installare il servizio:

    **installazione SVC**

    Il servizio scrive "servizio installato correttamente" nella console di se l'operazione ha esito positivo o un messaggio di errore in caso contrario.

    Se l'installazione del servizio ha esito positivo, il servizio viene visualizzato nell'applicazione dei **Servizi** . Si noti che il **nome** è impostato su "SvcName", la **Descrizione** e **lo stato** sono vuoti e il **tipo di avvio** è impostato su "Manual".

3.  Eseguire il comando seguente per avviare il servizio:

    **SvcControl avviare SvcName**

    Se l'operazione ha esito positivo, il programma di controllo del servizio scrive "avvio del servizio in sospeso..." e "il servizio è stato avviato correttamente" nella console. In caso contrario, il programma scrive un messaggio di errore nella console.

    Se il servizio viene avviato correttamente, **lo stato** è impostato su "avviato". Il codice nella funzione [*ServiceMain*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) viene eseguito dal gestore SCM. Se si verifica un errore, il servizio scriverà un messaggio di errore nel registro eventi. Questo messaggio include il nome della funzione che ha avuto esito negativo e il codice di errore restituito in caso di errore.

4.  Eseguire il comando seguente per aggiornare la descrizione del servizio:

    **svcconfig descrivere SvcName**

    Il programma di configurazione del servizio scrive "Descrizione servizio aggiornata" nella console di se l'operazione ha esito positivo o un messaggio di errore in caso contrario.

    Se l'aggiornamento ha esito positivo, la **Descrizione** è impostata su "Questa è una descrizione del test".

5.  Eseguire il comando seguente per eseguire una query sulla configurazione del servizio:

    **SvcName query svcconfig**

    Il programma di configurazione del servizio scrive le informazioni di configurazione del servizio nella console di se l'operazione ha esito positivo o un messaggio di errore in caso contrario.

6.  Eseguire il comando seguente per modificare il DACL del servizio:

    **SvcName DACL SvcControl**

    Il programma di configurazione del servizio scrive "DACL servizio aggiornato" alla console se l'operazione ha esito positivo o un messaggio di errore in caso contrario.

7.  Eseguire il comando seguente per disabilitare il servizio:

    **svcconfig Disabilita SvcName**

    Il programma di configurazione del servizio scrive "servizio disabilitato correttamente" nella console di se l'operazione ha esito positivo o un messaggio di errore in caso contrario.

    Se il servizio è stato disabilitato correttamente, il **tipo di avvio** è impostato su "disabilitato".

8.  Eseguire il comando seguente per abilitare il servizio:

    **svcconfig Abilita SvcName**

    Il programma di configurazione del servizio scrive "servizio abilitato correttamente" nella console se l'operazione ha esito positivo o un messaggio di errore in caso contrario.

    Se il servizio è stato abilitato correttamente, il **tipo di avvio** è impostato su "manuale".

9.  Eseguire il comando seguente per arrestare il servizio:

    **SvcControl arrestare SvcName**

    Se l'operazione ha esito positivo, il programma di controllo del servizio scrive "arresto servizio in sospeso..." e quindi "il servizio è stato arrestato correttamente" nella console. In caso contrario, il programma scrive un messaggio di errore nella console.

    Se il servizio viene arrestato correttamente, **lo stato** è vuoto.

    Se il servizio non viene arrestato, il programma di controllo del servizio scrive un messaggio di errore nel registro eventi che include il nome della funzione che ha avuto esito negativo e il codice di errore restituito in caso di errore.

10. Eseguire il comando seguente per eliminare il servizio:

    **svcconfig eliminare SvcName**

    Il programma di configurazione del servizio scrive "Servizio eliminato correttamente" nella console di se l'operazione ha esito positivo o un messaggio di errore in caso contrario.

    Se il servizio viene eliminato correttamente, non viene più visualizzato nell'applicazione **dei servizi** . Si noti che se si tenta di eliminare un servizio non arrestato, l'operazione ha esito positivo, ma il **tipo di avvio** è impostato su "disabilitato" e la voce del servizio verrà eliminata al riavvio del sistema o quando il servizio viene terminato tramite Gestione attività.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei servizi](using-services.md)
</dt> </dl>

 

 
