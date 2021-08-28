---
title: Profili di sistema
description: Profili di sistema
ms.assetid: 5f687aae-cf9b-4b2d-a3aa-d130b443fbf3
keywords:
- Windows Media Format SDK, profili di sistema
- Advanced Systems Format (ASF), profili di sistema
- ASF (Advanced Systems Format),profili di sistema
- Windows MEDIA Format SDK, ID profilo
- Advanced Systems Format (ASF), ID profilo
- ASF (Advanced Systems Format), ID profilo
- profili di sistema, elenco di
- ID profilo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6389f82e93a0b27c079bd75ded9eb7d35d78a380ab72d244c5443c07f4c9ed5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807741"
---
# <a name="system-profiles"></a>Profili di sistema

La tabella seguente contiene l'elenco completo dei profili di sistema supportati. Ogni profilo elencato ha un nome e un ID profilo. L'ID profilo è una costante impostata sul valore GUID assegnato al profilo di sistema. Per usare gli ID del profilo di sistema nel codice, è necessario includere wmsysprf.h nell'applicazione. Per esempi che illustrano come caricare un profilo di sistema, vedere [Per caricare un profilo di sistema](to-load-a-system-profile.md).

> [!IMPORTANT]
> I profili elencati di seguito usano tutti la versione 8 Windows codec Media Audio e Windows Media Video. Non sono disponibili profili di sistema predefiniti che usano i codec Windows Media 9 Series. È possibile creare un profilo Windows Media 9 Series usando un profilo versione 8 come punto di partenza. Per altre informazioni, vedere [Riutilizzo delle configurazioni dei flussi](reusing-stream-configurations.md).

 



| Nome profilo                                                                      | ID profilo                     | Descrizione                                                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Video multimediale 8 per PC pocket a colori (225 Kbps)                             | WMProfile \_ V80 \_ 255VideoPDA    | Usare questo profilo quando si creano file video per la riproduzione in Pocket PC a colori più veloci.                                                                                 |
| Windows Video multimediale 8 per PC pocket a colori (150 Kbps)                             | WMProfile \_ V80 \_ 150VideoPDA    | Usare questo profilo quando si creano file video per la riproduzione nella maggior parte dei Pocket PC.                                                                                         |
| Windows Video multimediale 8 per modem dial-up o ISDN a canale singolo (da 28,8 a 56 Kbps) | WMProfile \_ V80 \_ 28856VideoMBR  | Usare questo profilo a velocità in bit multipla per i destinatari di destinazione con modem dial-up o connessioni ISDN a canale singolo (la larghezza di banda è compresa tra 28,8 Kbps e 56 Kbps).        |
| Windows Video multimediale 8 per LAN, modem via cavo o xDSL (da 100 a 768 Kbps)             | WMProfile \_ V80 \_ 100768VideoMBR | Usare questo profilo a velocità in bit multipla per i destinatari con connessioni ISDN, LAN, modem via cavo o xDSL a doppio canale (la larghezza di banda è compresa tra 100 Kbps e 500 Kbps). |
| Windows Video multimediale 8 per modem dial-up o LAN (da 28,8 a 100 Kbps)                | WMProfile \_ V80 \_ 288100VideoMBR | Usare questo profilo a velocità in bit multipla per i destinatari con connessioni ISDN con modem remoto, LAN o a doppio canale (la larghezza di banda è compresa tra 28,8 e 100 Kbps).         |
| Windows Video multimediale 8 per modem dial-up (28,8 Kbps)                              | WMProfile \_ V80 \_ 288Video       | Usare questo profilo per il recapito audio/video a bassa velocità in bit su connessioni remote a 28,8 Kbps.                                                                          |
| Windows Video multimediale 8 per modem dial-up (56 Kbps)                                | WMProfile \_ V80 \_ 56Video        | Usare questo profilo per il recapito audio/video a bassa velocità in bit su connessioni remote a 56 Kbps.                                                                            |
| Windows Video multimediale 8 per la rete locale (100 Kbps)                           | WMProfile \_ V80 \_ 100Video       | Usare questo profilo per il recapito a velocità in bit media su connessioni ISDN, LAN o modem via cavo a doppio canale.                                                              |
| Windows Video multimediale 8 per la rete locale (256 Kbps)                           | WMProfile \_ V80 \_ 256Video       | Usare questo profilo per contenuti audio/video di alta qualità destinati alla riproduzione locale o per il download e la riproduzione.                                                     |
| Windows Video multimediale 8 per la rete locale (384 Kbps)                           | WMProfile \_ V80 \_ 384Video       | Usare questo profilo per contenuti audio/video di alta qualità destinati alla riproduzione locale o per il download e la riproduzione.                                                     |
| Windows Video multimediale 8 per la rete locale (768 Kbps)                           | WMProfile \_ V80 \_ 768Video       | Usare questo profilo per contenuti audio/video di alta qualità destinati alla riproduzione locale o per il download e la riproduzione.                                                     |
| Windows Video multimediale 8 per banda larga (NTSC, 700 Kbps)                              | WMProfile \_ V80 \_ 700NTSCVideo   | Usare questo profilo per contenuti audio/video di alta qualità destinati alla riproduzione locale o al download e alla riproduzione.                                                         |
| Windows Video multimediale 8 per banda larga (NTSC, 1400 Kbps)                             | WMProfile \_ V80 \_ 1400NTSCVideo  | Usare questo profilo per contenuti audio/video di alta qualità destinati alla riproduzione locale o per il download e la riproduzione.                                                     |
| Windows Video multimediale 8 per banda larga (PAL, 384 Kbps)                               | WMProfile \_ V80 \_ 384PALVideo    | Usare questo profilo per contenuti audio/video di alta qualità destinati alla riproduzione locale o per il download e la riproduzione.                                                     |
| Windows Video multimediale 8 per banda larga (PAL, 700 Kbps)                               | WMProfile \_ V80 \_ 700PALVideo    | Usare questo profilo per contenuti audio/video di alta qualità destinati alla riproduzione locale o per il download e la riproduzione.                                                     |
| Windows Audio multimediale 8 per modem remoto (Mono, 28,8 Kbps)                         | WMProfile \_ V80 \_ 288MonoAudio   | Usare questo profilo per contenuti radio e musicali (solo audio).                                                                                                          |
| Windows Audio multimediale 8 per modem remoto (FM Radio Stereo, 28,8 Kbps)              | WMProfile \_ V80 \_ 288StereoAudio | Usare questo profilo per contenuti radio e musicali (solo audio).                                                                                                          |
| Windows Audio multimediale 8 per modem remoto (32 Kbps)                                 | WMProfile \_ V80 \_ 32StereoAudio  | Usare questo profilo per contenuti radio e musicali (solo audio).                                                                                                          |
| Windows Audio multimediale 8 per modem dial-up (qualità QUASI CD, 48 Kbps)                | WMProfile \_ V80 \_ 48StereoAudio  | Usare per la radio, la musica e il contenuto audio per utilizzo generico.                                                                                                            |
| Windows Audio multimediale 8 per modem dial-up (qualità CD, 64 Kbps)                     | WMProfile \_ V80 \_ 64StereoAudio  | Usare questo profilo per i destinatari con connessioni Internet o LAN ad alta velocità.                                                                                  |
| Windows Audio multimediale 8 per ISDN (migliore della qualità cd, 96 Kbps)                  | WMProfile \_ V80 \_ 96StereoAudio  | Usare questo profilo per i destinatari con connessioni Internet o LAN ad alta velocità.                                                                                  |
| Windows Audio multimediale 8 per ISDN (migliore della qualità cd, 128 Kbps)                 | WMProfile \_ V80 \_ 128StereoAudio | Usare questo profilo per i destinatari con connessioni Internet o LAN ad alta velocità.                                                                                  |
| Windows Video multimediale 8 per modem remoto (nessun audio, 28,8 Kbps)                     | WMProfile \_ V80 \_ 288VideoOnly   | Usare questo profilo quando si crea contenuto solo video per destinatari di destinazione con modem dial-up.                                                                         |
| Windows Video multimediale 8 per modem remoto (nessun audio, 56 Kbps)                       | WMProfile \_ V80 \_ 56VideoOnly    | Usare questo profilo quando si crea contenuto solo video per destinatari di destinazione con modem dial-up.                                                                         |
| Windows Media 8 Fair Quality based VBR for Broadband                              | WMProfile \_ V80 \_ FAIRVBRVideo   | Profilo basato su qualità equa per contenuti VBR vincolati alla qualità.                                                                                     |
| Windows VBR basato su Media 8 di alta qualità per banda larga.                             | WMProfile \_ V80 \_ HIGHVBRVideo   | Profilo basato su qualità elevata o migliore per il contenuto VBR vincolato alla qualità.                                                                                     |
| Windows Media 8 Best Quality based VBR for Broadband.                             | WMProfile \_ V80 \_ BESTVBRVideo   | Profilo basato sulla qualità ottimale per il contenuto VBR vincolato alla qualità.                                                                                             |



 

I profili di sistema sono disponibili localizzati per lingue diverse dall'inglese. Per altre informazioni, vedere [Profili di sistema localizzati](localized-system-profiles.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IWMProfileManager::LoadProfileByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebyid)
</dt> <dt>

[**Interfaccia IWMProfileManager2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2)
</dt> <dt>

[**Uso dei profili**](working-with-profiles.md)
</dt> </dl>

 

 




