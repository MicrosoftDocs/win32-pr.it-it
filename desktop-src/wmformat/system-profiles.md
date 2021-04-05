---
title: Profili di sistema
description: Profili di sistema
ms.assetid: 5f687aae-cf9b-4b2d-a3aa-d130b443fbf3
keywords:
- Windows Media Format SDK, profili di sistema
- ASF (Advanced Systems Format), profili di sistema
- ASF (formato avanzato dei sistemi), profili di sistema
- Windows Media Format SDK, ID profilo
- ASF (Advanced Systems Format), ID profilo
- ASF (formato avanzato dei sistemi), ID profilo
- profili di sistema, elenco di
- ID profilo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeca66023e6de6aba9c07a6bcb84a73756e316a8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723583"
---
# <a name="system-profiles"></a>Profili di sistema

La tabella seguente contiene l'elenco completo dei profili di sistema supportati. Ogni profilo elencato ha un nome e un ID profilo. L'ID del profilo è una costante impostata sul valore GUID assegnato al profilo di sistema. Per usare gli ID profilo di sistema nel codice, è necessario includere wmsysprf. h nell'applicazione. Per esempi che illustrano come caricare un profilo di sistema, vedere [per caricare un profilo di sistema](to-load-a-system-profile.md).

> [!IMPORTANT]
> I profili elencati di seguito usano tutti la versione 8 Windows Media Audio e i codec Windows Media Video. Non esistono profili di sistema predefiniti che usano i codec della serie Windows Media 9. È possibile creare un profilo della serie Windows Media 9 usando un profilo della versione 8 come punto di partenza. Per ulteriori informazioni, vedere [riutilizzo delle configurazioni di flusso](reusing-stream-configurations.md).

 



| Nome profilo                                                                      | ID profilo                     | Descrizione                                                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Media Video 8 per i Pocket PC a colori (225 kbps)                             | WMProfile \_ V80 \_ 255VideoPDA    | Usare questo profilo durante la creazione di file video per la riproduzione in Pocket PC più veloci.                                                                                 |
| Windows Media Video 8 per i Pocket PC a colori (150 Kbps)                             | WMProfile \_ V80 \_ 150VideoPDA    | Usare questo profilo durante la creazione di file video per la riproduzione nella maggior parte dei Pocket PC.                                                                                         |
| Windows Media Video 8 per modem remote o ISDN a canale singolo (da 28,8 a 56 Kbps) | WMProfile \_ V80 \_ 28856VideoMBR  | Usare questo profilo della velocità a più bit per i destinatari con modem di connessione remota o connessioni ISDN a canale singolo (la larghezza di banda è compresa tra 28,8 e 56 Kbps).        |
| Windows Media Video 8 per LAN, modem via cavo o xDSL (da 100 a 768 Kbps)             | WMProfile \_ V80 \_ 100768VideoMBR | Usare questo profilo della velocità a più bit per i destinatari con connessioni ISDN Dual Channel, LAN, modem via cavo o xDSL (la larghezza di banda è compresa tra 100 kbps e 500 Kbps). |
| Windows Media Video 8 per modem di connessione remota o LAN (da 28,8 a 100 Kbps)                | WMProfile \_ V80 \_ 288100VideoMBR | Usare questo profilo della velocità a più bit per i destinatari con connessioni remote modem, LAN o ISDN a doppio canale (la larghezza di banda è compresa tra 28,8 e 100 Kbps).         |
| Windows Media Video 8 per modem di connessione remota (28,8 Kbps)                              | WMProfile \_ V80 \_ 288Video       | Usare questo profilo per il recapito audio/video con velocità in bit ridotta oltre le connessioni remote a 28,8 kbps.                                                                          |
| Windows Media Video 8 per modem di connessione remota (56 Kbps)                                | WMProfile \_ V80 \_ 56Video        | Usare questo profilo per il recapito audio/video con velocità in bit ridotta oltre le connessioni remote a 56 Kbps.                                                                            |
| Windows Media Video 8 per la rete locale (100 Kbps)                           | WMProfile \_ V80 \_ 100Video       | Usare questo profilo per il recapito a velocità in bit media su connessioni modem ISDN, LAN o cablaggio Dual Channel.                                                              |
| Windows Media Video 8 per la rete locale (256 Kbps)                           | WMProfile \_ V80 \_ 256Video       | Usare questo profilo per contenuti audio/video di alta qualità destinati alla riproduzione locale o per il download e la riproduzione.                                                     |
| Windows Media Video 8 per la rete locale (384 Kbps)                           | WMProfile \_ V80 \_ 384Video       | Usare questo profilo per contenuti audio/video di alta qualità destinati alla riproduzione locale o per il download e la riproduzione.                                                     |
| Windows Media Video 8 per la rete locale (768 Kbps)                           | WMProfile \_ V80 \_ 768Video       | Usare questo profilo per contenuti audio/video di alta qualità destinati alla riproduzione locale o per il download e la riproduzione.                                                     |
| Windows Media Video 8 per la banda larga (NTSC, 700 Kbps)                              | WMProfile \_ V80 \_ 700NTSCVideo   | Usare questo profilo per contenuti audio/video di alta qualità destinati alla riproduzione locale o al download e alla riproduzione.                                                         |
| Windows Media Video 8 per la banda larga (NTSC, 1400 Kbps)                             | WMProfile \_ V80 \_ 1400NTSCVideo  | Usare questo profilo per contenuti audio/video di alta qualità destinati alla riproduzione locale o per il download e la riproduzione.                                                     |
| Windows Media Video 8 per la banda larga (PAL, 384 Kbps)                               | WMProfile \_ V80 \_ 384PALVideo    | Usare questo profilo per contenuti audio/video di alta qualità destinati alla riproduzione locale o per il download e la riproduzione.                                                     |
| Windows Media Video 8 per la banda larga (PAL, 700 Kbps)                               | WMProfile \_ V80 \_ 700PALVideo    | Usare questo profilo per contenuti audio/video di alta qualità destinati alla riproduzione locale o per il download e la riproduzione.                                                     |
| Windows Media Audio 8 per modem remoto (mono, 28,8 Kbps)                         | WMProfile \_ V80 \_ 288MonoAudio   | Usare questo profilo per il contenuto radio e musicale (solo audio).                                                                                                          |
| Windows Media Audio 8 per modem remoto (FM radio stereo, 28,8 Kbps)              | WMProfile \_ V80 \_ 288StereoAudio | Usare questo profilo per il contenuto radio e musicale (solo audio).                                                                                                          |
| Windows Media Audio 8 per modem remoto (32 Kbps)                                 | WMProfile \_ V80 \_ 32StereoAudio  | Usare questo profilo per il contenuto radio e musicale (solo audio).                                                                                                          |
| Windows Media Audio 8 per modem remoto (near CD Quality, 48 kbps)                | WMProfile \_ V80 \_ 48StereoAudio  | Da usare per contenuti audio per radio, musica e per utilizzo generico.                                                                                                            |
| Windows Media Audio 8 per modem remoto (qualità CD, 64 Kbps)                     | WMProfile \_ V80 \_ 64StereoAudio  | Usare questo profilo per i destinatari con connessioni Internet o LAN ad alta velocità.                                                                                  |
| Windows Media Audio 8 per ISDN (migliore qualità del CD, 96 Kbps)                  | WMProfile \_ V80 \_ 96StereoAudio  | Usare questo profilo per i destinatari con connessioni Internet o LAN ad alta velocità.                                                                                  |
| Windows Media Audio 8 per ISDN (migliore qualità del CD, 128 Kbps)                 | WMProfile \_ V80 \_ 128StereoAudio | Usare questo profilo per i destinatari con connessioni Internet o LAN ad alta velocità.                                                                                  |
| Windows Media Video 8 per modem remoto (senza audio, 28,8 Kbps)                     | WMProfile \_ V80 \_ 288VideoOnly   | Usare questo profilo quando si crea contenuto solo video per destinatari con modem di connessione remota.                                                                         |
| Windows Media Video 8 per modem remoto (senza audio, 56 Kbps)                       | WMProfile \_ V80 \_ 56VideoOnly    | Usare questo profilo quando si crea contenuto solo video per destinatari con modem di connessione remota.                                                                         |
| Windows Media 8 VBR basato sulla qualità corretta per la banda larga                              | WMProfile \_ V80 \_ FAIRVBRVideo   | Profilo basato su qualità elevata per il contenuto VBR con una qualità vincolata.                                                                                     |
| Windows Media 8 VBR basato su alta qualità per la banda larga.                             | WMProfile \_ V80 \_ HIGHVBRVideo   | Profilo massimo per la qualità migliore per il contenuto VBR con una qualità vincolata.                                                                                     |
| Windows Media 8 VBR basato sulla qualità migliore per la banda larga.                             | WMProfile \_ V80 \_ BESTVBRVideo   | Profilo migliore per la qualità per il contenuto VBR con una qualità vincolata.                                                                                             |



 

I profili di sistema sono disponibili localizzati per lingue diverse dall'inglese. Per ulteriori informazioni, vedere [profili di sistema localizzati](localized-system-profiles.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IWMProfileManager::LoadProfileByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebyid)
</dt> <dt>

[**Interfaccia IWMProfileManager2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2)
</dt> <dt>

[**Utilizzo dei profili**](working-with-profiles.md)
</dt> </dl>

 

 




