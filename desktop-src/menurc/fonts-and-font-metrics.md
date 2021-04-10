---
title: Tipi di carattere e metriche di testo
description: In questo argomento vengono illustrati i tipi di carattere del contorno forniti da Windows, i valori delle metriche dei caratteri che possono cambiare tra le versioni di Windows e le linee guida per l'utilizzo delle metriche dei tipi di carattere nelle applicazioni desktop.
ms.assetid: B195154D-0168-4C5E-9CFB-AE7EF63D5F42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da27d4eb5f34f5a88e4a0e3e866f9a14784c3895
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963073"
---
# <a name="fonts-and-text-metrics"></a>Tipi di carattere e metriche di testo

In questo argomento vengono illustrati i tipi di carattere del contorno forniti da Windows, i valori delle metriche dei caratteri che possono cambiare tra le versioni di Windows e le linee guida per l'utilizzo delle metriche dei tipi di carattere nelle applicazioni desktop.

-   Per informazioni specifiche per le metriche dei tipi di carattere in DirectWrite, vedere [metriche del testo](/windows/desktop/DirectWrite/text-metrics).
-   Per informazioni dettagliate sulla gestione del testo nelle app con GDI, vedere gli argomenti in [tipi di carattere e testo](/windows/desktop/gdi/fonts-and-text).

Per informazioni più dettagliate sull'utilizzo dei tipi di carattere e sulle specifiche dei tipi, vedere il [sito Microsoft Typography](https://www.microsoft.com/typography/default.mspx).

## <a name="available-fonts"></a>Tipi di carattere disponibili

I tipi di carattere del contorno forniti con Windows vengono forniti come tipi di carattere OpenType con le strutture TrueType (Windows supporta anche i tipi di carattere OpenType nel formato CFF). Per gli elenchi di tutti i tipi di carattere forniti da Windows, vedere [Microsoft Typography: tipi di carattere per prodotto o famiglia](https://www.microsoft.com/typography/fonts/default.aspx). Tutti i tipi di carattere del contorno di Windows sono conformi alla versione più recente della [specifica OpenType](https://www.microsoft.com/typography/otspec/).

Per un elenco di tutti i tipi di carattere dell'interfaccia utente correnti e legacy, vedere le [metriche dei tipi di carattere bloccati](#locked-font-metrics) di seguito.

## <a name="font-modifications"></a>Modifiche dei tipi di carattere

Per garantire la compatibilità con le versioni precedenti, i tipi di carattere vengono rimossi raramente da Windows. Tuttavia, i tipi di carattere vengono spesso modificati. Le modifiche possono includere l'aggiunta di caratteri, il ridisegno di caratteri esistenti, la modifica di hint o l'aggiunta o la modifica del supporto per funzionalità OpenType avanzate e la definizione di script complessi.

### <a name="locked-font-metrics"></a>Metriche dei tipi di carattere bloccati

Si noti che alcuni valori associati ai tipi di carattere dell'interfaccia utente e ai tipi di carattere predefiniti usati nelle app Microsoft sono bloccati. I tipi di carattere dell'interfaccia utente vengono usati per eseguire il rendering di elementi dell'interfaccia utente quali didascalie, finestre di dialogo e menu Vengono apportate poche modifiche a questi tipi di carattere, data la visibilità elevata e l'uso frequente. Tuttavia, poiché i valori segnalati associati a questi tipi di carattere sono bloccati, è possibile che si verifichino discrepanze tra i valori dei tipi di carattere restituiti ed effettivi

I valori segnalati seguenti sono bloccati per l'interfaccia utente e i tipi di carattere predefiniti e potrebbero essere segnalati in modo non corretto:

-   Questi valori della [tabella OS/2](https://www.microsoft.com/typography/otspec/os2.htm)del tipo di carattere:
    -   xAvgCharWidth
    -   sTypoLineGap
    -   sTypoAscender
    -   sTypoDescender
    -   usWinAscent
    -   usWinDescent
-   Valore [unitsPerEm](https://www.microsoft.com/typography/otspec/head.htm) impostato nell'intestazione del tipo di carattere
-   Valori della [Tabella metrica dispositivi verticali (VDMX)](https://www.microsoft.com/typography/otspec/vdmx.htm)
-   Larghezze di avanzamento per i singoli glifi

Ecco un elenco dei tipi di carattere dell'interfaccia utente forniti con Windows 8.1 (interessati dai valori bloccati):

| Nome script                   | Tipo di carattere dell'interfaccia utente               |
|-------------------------------|-----------------------|
| Arabo                        | Segoe UI              |
| Armeno                      | Segoe UI              |
| Bangla (in precedenza Bengali)     | Nirmala UI            |
| Bopomofo                      | Microsoft JhengHei UI |
| Braille                       | Segoe UI Symbol       |
| Buginese                      | Leelawadee UI         |
| Sillabico aborigeno canadese | Gadugi                |
| Cherokee                      | Gadugi                |
| Copto                        | Segoe UI Symbol       |
| Cinese (semplificato)          | Microsoft YaHei UI    |
| Cinese (tradizionale)         | Microsoft JhengHei UI |
| Cirillico                      | Segoe UI              |
| Devanagari                    | Nirmala UI            |
| Deseret                       | Segoe UI Symbol       |
| Etiope                      | Ebrima                |
| Georgiano                      | Segoe UI              |
| Glagolitico                    | Segoe UI Symbol       |
| Gothic                        | Segoe UI Symbol       |
| Greco                         | Segoe UI              |
| Gujarati                      | Nirmala UI            |
| Gurmukhi                      | Nirmala UI            |
| Ebraico                        | Segoe UI              |
| Corsivo precedente                    | Segoe UI Symbol       |
| Giavanese                      | Testo giavanese         |
| Giapponese                      | Interfaccia utente di Meiryo             |
| Kannada                       | Interfaccia utente di Mirmala            |
| Khmer                         | Leelawadee UI         |
| Coreano                        | Malgun Gothic         |
| Lao                           | Leelawadee UI         |
| Latino                         | Segoe UI              |
| Malayalam                     | Nirmala UI            |
| Mongolo                     | Mongolian Baiti       |
| Myanmar                       | Myanmar Text          |
| Modellazione N'Ko                          | Ebrima                |
| Ogamico                         | Segoe UI Symbol       |
| Chiki OL                      | Nirmala UI            |
| Vecchio turco                    | Segoe UI Symbol       |
| Odia (in precedenza Oriya)         | Nirmala UI            |
| Osmanya                       | Ebrima                |
| Carattere phags-pa                      | Microsoft PhagsPa     |
| Runico                         | Segoe UI Symbol       |
| Sora Sompeng                  | Nirmala UI            |
| Singalese                       | Nirmala UI            |
| Siriaco                        | Estrangelo Edessa     |
| Tai le                        | Microsoft Tai Le      |
| Nuovo tai lue                   | Microsoft New Tai Lue |
| Tamil                         | Nirmala UI            |
| Telugu                        | Nirmala UI            |
| Tifinagh                      | Ebrima                |
| Thaana                        | MV Boli               |
| Thai                          | Leelawadee UI         |
| Tibetano                       | Microsoft Himalaya    |
| Vai                           | Ebrima                |
| Yi                            | Microsoft Yi Baiti    |



 

Ecco un elenco dei tipi di carattere legacy dell'interfaccia utente che sono interessati anche dai valori bloccati:

| Nome dello script (legacy)          | Tipo di carattere dell'interfaccia utente (legacy)               |
|-------------------------------|--------------------------------|
| Bangla (in precedenza Bengali)     | Vrinda                         |
| Sillabico aborigeno canadese | Eufemia                       |
| Cherokee                      | Plantageneto                    |
| Cinese (semplificato)          | Microsoft YaHei e SimSun     |
| Cinese (tradizionale)         | MingLiU e Microsoft JhengHei |
| Devanagari                    | Mangal                         |
| Lingue europee            | Tahoma                         |
| Gujarati                      | Shruti                         |
| Gurmukhi                      | Ratti                          |
| Giapponese                      | Interfaccia utente di Meiryo e MS Gothic        |
| Kannada                       | Tunga                          |
| Khmer                         | Khmer                          |
| Coreano                        | Gulim                          |
| Lao                           | Interfaccia utente di Lao                         |
| Malayalam                     | Kartika                        |
| Lingue mediorientali      | Tahoma                         |
| Odia (in precedenza Oriya)         | Kalinga                        |
| Singalese                     | Pota                   |
| Tamil                         | Lalucci e Vijaya               |
| Telugu                        | Gautami                        |
| Thai                          | Leelawadee e Tahoma          |



 

Questi tipi di carattere vengono usati come impostazioni predefinite nelle app Microsoft e sono interessati anche dai valori bloccati:

-   Arial
-   Calibri
-   Cambria
-   Consolas
-   Courier New
-   MS Mincho
-   Times New Roman
-   Verdana

### <a name="dynamic-font-metrics"></a>Metriche dei tipi di carattere dinamici

Oltre alle metriche bloccate sopra elencate, i valori dei tipi di carattere vengono segnalati in modo accurato. Se un tipo di carattere viene modificato in una nuova versione di Windows, i valori dei tipi di carattere dinamici variano tra i nuovi e quelli precedenti. Ad esempio, quando un glifo viene aggiunto a un tipo di carattere, è possibile che i valori nell'intestazione del tipo di carattere cambino. Il ritaglio può verificarsi se questi valori (che includono xMin, xMax, yMin e yMax e segnalano il rettangolo di delimitazione minimo e massimo per i glifi del tipo di carattere) sono bloccati e non segnalano valori reali.

> [!IMPORTANT]
> Se si usano valori di tipo carattere dinamici nell'app, ad esempio quelli in [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica), questi valori verranno modificati se i tipi di carattere vengono modificati nelle versioni future di Windows. Non usare questi valori effettivi nelle situazioni in cui il testo deve rimanere statico.

 

## <a name="guidelines-for-using-font-metrics"></a>Linee guida per l'uso delle metriche dei tipi di carattere

-   Calcolare la metrica dello schermo e la metrica del tipo di carattere, ad esempio la larghezza media, quando viene avviata un'app e usare questi valori per il layout dell'app. In questo modo verrà fornito un rendering coerente e il layout risponderà alle modifiche nei tipi di carattere o al fallback del tipo di carattere. Per una panoramica del fallback dei tipi di carattere e del collegamento dei tipi di carattere, vedere la pagina relativa alla [globalizzazione Step by Step: caratteri](https://msdn.microsoft.com/goglobal/bb688134.aspx). Vedere [uso del fallback dei tipi di carattere](/windows/desktop/Intl/using-font-fallback) per le informazioni specifiche di Uniscribe.
    -   Per calcolare una metrica di base, eseguire il rendering del testo rappresentativo per il linguaggio o lo script desiderato.
    -   Per i controlli che contengono solo una singola riga di testo non incapsulato, impostarli in modo da adattarsi alla larghezza completa del testo non tagliato.
    -   Per i controlli con più righe, ottenere la lunghezza totale, dividere per la lunghezza del carattere e avere una larghezza a tinta unita da usare. Si noti che questa operazione è più complessa per gli script complessi in cui un singolo carattere "character" per il lettore può essere costituito da più punti di codice.
-   Usare sTypoAscender, sTypoDescender e unitsPerEm (dalla [tabella OS/2](https://www.microsoft.com/typography/otspec/os2.htm)) per calcolare la spaziatura verticale. sTypoAscender viene usato per determinare l'offset ottimale dalla parte superiore di un frame di testo alla prima baseline e sTypoDescender determina l'offset ottimale dalla parte inferiore di un frame di testo fino all'ultima Baseline.
-   Se si usa DirectWrite, creare un layout usando [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout). **IDWriteTextLayout** fornisce   +  lineGap di **decrescente** ascendenti  +   nel layout naturale. È possibile accedere a questi valori specifici con la [**\_ \_ metrica del tipo di carattere DWrite**](/windows/desktop/api/dwrite/ns-dwrite-dwrite_font_metrics). Per informazioni su questa interfaccia, vedere [formattazione e layout del testo](/windows/desktop/DirectWrite/text-formatting-and-layout).
-   Se si usa GDI, eseguire il rendering dallo schermo, quindi controllare il layout (ad esempio, la lunghezza di riga o i caratteri per riga) e ricalcolare i parametri di layout finali usati nel rendering effettivo.
-   Non compilare i layout in modo statico in base a valori specifici per versioni particolari dei tipi di carattere. I valori effettivi possono variare da release a Release.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[**\_metriche dei tipi di carattere DWrite \_**](/windows/desktop/api/dwrite/ns-dwrite-dwrite_font_metrics)
</dt> <dt>

[**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)
</dt> <dt>

[unitsPerEm](https://www.microsoft.com/typography/otspec/head.htm)
</dt> <dt>

[Tabella OS/2](https://www.microsoft.com/typography/otspec/os2.htm)
</dt> <dt>

[Tabella metrica dispositivi verticali (VDMX)](https://www.microsoft.com/typography/otspec/vdmx.htm)
</dt> <dt>

[Microsoft Typography: tipi di carattere per prodotto o famiglia](https://www.microsoft.com/typography/fonts/default.aspx)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Metrica testo (DirectWrite)](/windows/desktop/DirectWrite/text-metrics)
</dt> <dt>

[Tipi di carattere e testo (GDI)](/windows/desktop/gdi/fonts-and-text)
</dt> <dt>

[Elementi tipografici Microsoft](https://www.microsoft.com/typography/default.mspx)
</dt> </dl>

 

 