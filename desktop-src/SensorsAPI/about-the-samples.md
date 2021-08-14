---
description: L Windows SDK include esempi di codice e strumenti utili per comprendere e usare la piattaforma sensore e posizione Windows e le API correlate.
ms.assetid: e31174f6-1c2b-4d97-b6b6-e54825ff47f5
title: Informazioni su esempi e strumenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5eecd388323ae8a548fcfefbc116224125b4b137f85231c56ea66235b3233fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890321"
---
# <a name="about-the-samples-and-tools"></a>Informazioni su esempi e strumenti

L Windows SDK include esempi di codice e strumenti utili per comprendere e usare la piattaforma sensore e posizione Windows e le API correlate.

## <a name="samples"></a>Esempi

L Windows SDK include gli esempi di API Sensor seguenti. Gli esempi dell'API Sensor sono disponibili nella cartella \\ Samples \\ winui Sensors, in cui è stato installato \\ Windows SDK. Ad esempio, se è stato installato Windows SDK nell'unità C, gli esempi si trovano nella cartella seguente: C: \\ Programmi Microsoft SDK Windows \\ \\ \\ v7.0 \\ Samples \\ winui \\ Sensors.



| Nome esempio       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AmbientLightAware | Questo esempio MFC illustra come usare l'API Sensor leggendo i dati dai sensori di luce ambientale nel computer e modificando le dimensioni del testo in base alle condizioni di illuminazione. È possibile visualizzare il codice che illustra come gestire gli eventi e come richiedere le autorizzazioni utente. È anche possibile vedere un esempio di come gestire l'interfaccia utente in base a diverse condizioni di illuminazione. Per altre informazioni, vedere [Creazione Light-Aware interfacce utente.](creating-light-aware-user-interfaces.md)<br/> Per compilare questo esempio è necessario Visual Studio 2008.<br/> |



 

Per altre informazioni, vedere il file denominato ReadMe.txt incluso nell'esempio.

È anche possibile scaricare l'esempio AmbientLightAware dalla raccolta di codice. Per altre informazioni, vedere la pagina di download [di Ambient Light Aware.](/samples/browse/?redirectedfrom=MSDN-samples)

## <a name="tools"></a>Strumenti

L Windows SDK include un sensore di luce virtuale che è possibile usare per simulare un dispositivo sensore di luce basato su hardware. È possibile usare questo strumento per fornire dati all'esempio AmbientLightAware per verificare il funzionamento del codice nell'esempio.

La tabella seguente descrive i file che è necessario usare per eseguire il sensore di luce virtuale. È possibile trovare questi file nella cartella denominata Bin, in cui è stato installato Windows SDK. Ad esempio, se l'SDK di Windows è stato installato nell'unità C in un computer a 32 bit, i file del sensore di luce virtuale si trovano nella cartella seguente: C: Programmi \\ \\ Microsoft SDK Windows \\ \\ v7.0 \\ Bin. Nei computer a 64 bit è necessario usare la versione a 64 bit dello strumento. In Windows SDK, gli strumenti a 64 bit si trovano nella sottocartella denominata x64.



| Nome file                    | Descrizione                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| VirtualLightSensor.exe       | Questo programma fornisce un controllo dispositivo di scorrimento che consente di modificare il livello dei dati luminosi segnalati dal sensore virtuale. |
| VirtualLightSensorDriver.dll | Il driver del sensore logico che simula un sensore di luce.                                                                       |
| VirtualLightSensorDriver.inf | File INF per il driver del sensore di luce virtuale.                                                                              |



 

### <a name="installing-the-virtual-light-sensor"></a>Installazione del sensore di luce virtuale

Prima di usare l'applicazione sensore di luce virtuale, è necessario installare il driver del sensore logico. Seguire questa procedura:

1.  Aprire una finestra di comando come amministratore.
2.  Passare alla cartella Windows SDK Bin.
3.  Digitare **pnputil -a VirtualLightSensorDriver.inf**.
4.  Quando richiesto, fare clic **su Installa il software del driver comunque**.
5.  Attendere che la finestra di comando segnala che il driver è stato installato correttamente.

### <a name="running-the-virtual-light-sensor"></a>Esecuzione del sensore di luce virtuale

Per eseguire il sensore di luce virtuale, è sufficiente fare doppio clic sul file .exe virtuale. Assicurarsi di abilitare il sensore, quando richiesto.

Quando si esegue il programma, è possibile notare che si verifica un ritardo prima che il sensore diventi disponibile. L'interfaccia utente del sensore di luce virtuale visualizza il messaggio "Waiting" nella barra del titolo mentre il gestore del sensore logico crea un nodo di dispositivo per il sensore logico. Dopo che il messaggio in attesa si è allontanato, è possibile usare il dispositivo di scorrimento per impostare il livello di output di lusso per il sensore di luce virtuale.

L'immagine seguente mostra l'interfaccia utente del sensore di luce virtuale nello stato pronto.

![Interfaccia utente del sensore di luce virtuale](images/virtuallightsensor.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui sensori logici](about-logical-sensors.md)
</dt> <dt>

[**LUCE \_ CATEGORIA \_ SENSORE**](sensor-category-light.md)
</dt> </dl>

 

