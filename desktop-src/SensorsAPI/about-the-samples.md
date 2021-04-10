---
description: Il Windows SDK include utili esempi di codice e strumenti che consentono di comprendere e usare la piattaforma del sensore e della posizione di Windows e le API correlate.
ms.assetid: e31174f6-1c2b-4d97-b6b6-e54825ff47f5
title: Informazioni sugli esempi e sugli strumenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6126ec5e07829cfd17c2b07313bb104140c6fee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884262"
---
# <a name="about-the-samples-and-tools"></a>Informazioni sugli esempi e sugli strumenti

Il Windows SDK include utili esempi di codice e strumenti che consentono di comprendere e usare la piattaforma del sensore e della posizione di Windows e le API correlate.

## <a name="samples"></a>Esempi

Il Windows SDK include i seguenti esempi di API per i sensori. È possibile trovare gli esempi di API per i sensori nella cartella denominata \\ Samples \\ WinUI \\ Sensors, in cui è stato installato il Windows SDK. Se, ad esempio, è stato installato il Windows SDK sull'unità C, gli esempi sono disponibili nella cartella seguente: C: \\ programmi \\ Microsoft SDK \\ Windows \\ v 7.0 \\ esempi \\ WinUI \\ sensori.



| Nome esempio       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AmbientLightAware | Questo esempio MFC illustra come usare l'API del sensore leggendo i dati dai sensori di luce di ambiente sul computer e modificando le dimensioni del testo in base alle condizioni di illuminazione. È possibile visualizzare il codice che illustra come gestire gli eventi e come richiedere le autorizzazioni utente. È anche possibile vedere un esempio di come gestire l'interfaccia utente in base a condizioni di illuminazione diverse. Per ulteriori informazioni, vedere [creazione di Light-Aware interfacce utente](creating-light-aware-user-interfaces.md).<br/> Per compilare questo esempio, è necessario che Visual Studio 2008 sia installato.<br/> |



 

Per ulteriori informazioni, vedere il file denominato ReadMe.txt incluso nell'esempio.

È anche possibile scaricare l'esempio AmbientLightAware da Code Gallery. Per ulteriori informazioni, vedere la pagina di download con rilevamento [chiaro di ambiente](/samples/browse/?redirectedfrom=MSDN-samples) .

## <a name="tools"></a>Strumenti

Il Windows SDK include un sensore di luce virtuale che è possibile usare per simulare un dispositivo sensore di luce basato su hardware. È possibile usare questo strumento per fornire dati all'esempio AmbientLightAware per vedere come funziona il codice nell'esempio.

La tabella seguente descrive i file che è necessario usare per eseguire il sensore di luce virtuale. È possibile trovare questi file nella cartella denominata bin, in cui è stato installato il Windows SDK. Se, ad esempio, è stato installato il Windows SDK sull'unità C in un computer a 32 bit, i file del sensore di luce virtuale saranno disponibili nella cartella seguente: C: \\ programmi \\ Microsoft SDK \\ Windows \\ v 7.0 \\ bin. Nei computer a 64 bit, è necessario utilizzare la versione a 64 bit dello strumento. Nella Windows SDK gli strumenti a 64 bit si trovano nella sottocartella denominata x64.



| Nome file                    | Descrizione                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| VirtualLightSensor.exe       | Questo programma fornisce un controllo dispositivo di scorrimento che consente di modificare il livello dei dati leggeri segnalati dal sensore virtuale. |
| VirtualLightSensorDriver.dll | Driver del sensore logico che simula un sensore di luminosità.                                                                       |
| VirtualLightSensorDriver. inf | File INF per il driver del sensore di luce virtuale.                                                                              |



 

### <a name="installing-the-virtual-light-sensor"></a>Installazione del sensore di luce virtuale

Prima di usare l'applicazione Virtual Light Sensor, è necessario installare il driver del sensore logico. A tale scopo, seguire questa procedura:

1.  Aprire una finestra di comando come amministratore.
2.  Passare alla cartella bin Windows SDK.
3.  Digitare **pnputil-a VirtualLightSensorDriver. inf**.
4.  Quando richiesto, fare clic su **installa comunque il software driver**.
5.  Attendere che la finestra di comando segnali che il driver è stato installato correttamente.

### <a name="running-the-virtual-light-sensor"></a>Esecuzione del sensore di luce virtuale

Per eseguire il sensore di luce virtuale, è sufficiente fare doppio clic sul file exe. Assicurarsi di abilitare il sensore quando richiesto.

Quando si esegue il programma, è possibile notare che si verifica un ritardo prima che il sensore diventi disponibile. L'interfaccia utente del sensore di luce virtuale visualizzerà il messaggio "Waiting" sulla barra del titolo mentre Gestione sensori logici creerà un nodo del dispositivo per il sensore logico. Quando il messaggio in attesa scompare, è possibile usare il dispositivo di scorrimento per impostare il livello di output Lux per il sensore di luce virtuale.

La figura seguente mostra l'interfaccia utente del sensore di luce virtuale nello stato pronto.

![interfaccia utente del sensore di luce virtuale](images/virtuallightsensor.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui sensori logici](about-logical-sensors.md)
</dt> <dt>

[**\_categoria sensore \_ chiaro**](sensor-category-light.md)
</dt> </dl>

 

