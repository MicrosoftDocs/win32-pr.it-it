---
title: Using RC (The RC Command Line) (Uso di RC - Riga di comando RC)
description: Per avviare RC, usare il comando seguente.
ms.assetid: da087e15-ecb5-4d03-b534-be872cf7d8b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e560ebee4312dccc2463caf123f05a5ad9831cd293c9976350e6de7ee13cb64a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971920"
---
# <a name="using-rc-the-rc-command-line"></a>Using RC (The RC Command Line) (Uso di RC - Riga di comando RC)

Per avviare RC, usare il comando seguente.

**RC** \[ *opzioni* \] *file di script*

Il *parametro script-file* specifica il nome del file di definizione delle risorse che contiene i nomi, i tipi, i nomi dei file e le descrizioni delle risorse da compilare.

RC può generare file di risorse separati per le applicazioni con risorse indipendenti dalla lingua e specifiche della lingua. Gli sviluppatori possono usare un [file](/windows/desktop/Intl/preparing-resources) di configurazione delle risorse o impostare opzioni della riga di comando per selezionare quali tipi di risorse ed elementi sono risorse non localizzabili del file indipendente dalla lingua [(LN)](/windows/desktop/Intl/mui-resource-management) e quali sono risorse localizzabili di file MUI specifici del linguaggio. Per altre informazioni, vedere [l'interfaccia utente multilingue](/windows/desktop/Intl/multilingual-user-interface).

Il *parametro options* può essere una o più delle opzioni della riga di comando seguenti.

## <a name="options"></a>Opzioni

<dl> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Visualizza un elenco di opzioni della riga di comando.

</dd> <dt>

<span id="_c"></span><span id="_C"></span>**/c**
</dt> <dd>

Definisce una tabella codici usata dalla conversione NLS.

</dd> <dt>

<span id="_d"></span><span id="_D"></span>**/d**
</dt> <dd>

Definisce un simbolo per il preprocessore che è possibile testare con la [**\# direttiva ifdef.**](-ifdef.md)

</dd> <dt>

<span id="_fm_mresname"></span><span id="_FM_MRESNAME"></span>**/fm** *mresname*
</dt> <dd>

RC crea un solo oggetto indipendente dalla lingua. FILE RES e un file MUI (Language-Dependent Language). FILE RES con *file di script*. Questa opzione deve essere usata insieme **all'opzione /fo** *resname.* Il nome RC è indipendente dalla lingua. *Resname.res* del file RES e il nome muI (Language-Dependent Language-Dependent). File RES *mresname.res*.

**Windows Server 2003 e Windows XP/2000:** Questa opzione non è disponibile senza usare anche le [**funzioni LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) e [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) in un sistema aggiornato.

</dd> <dt>

<span id="_fo_resname"></span><span id="_FO_RESNAME"></span>**/fo** *resname*
</dt> <dd>

RC crea un oggetto . File RES denominato *resname usando* *script-file*.

Se è **impostata anche l'opzione /fm** *mresname,* RC crea un oggetto indipendente dalla lingua. FILE RES e un file MUI (Language-Dependent Language). FILE RES.

**Windows Server 2003 e Windows XP/2000:** Questa opzione non è disponibile senza usare anche le [**funzioni LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) e [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) in un sistema aggiornato.

</dd> <dt>

<span id="_g1"></span><span id="_G1"></span>**/g1**
</dt> <dd>

Se /g1, è impostato, RC genera un file MUI se l'unica risorsa localizzabile inclusa nel file MUI è una risorsa di versione. Se /g1 non è impostato, RC non genererà un file MUI se l'unica risorsa localizzabile inclusa nel file MUI è una risorsa di versione.

</dd> <dt>

<span id="_h"></span><span id="_H"></span>**/h**
</dt> <dd>

Visualizza l'elenco delle opzioni della riga di comando.

</dd> <dt>

<span id="_I"></span><span id="_i"></span>**/i**
</dt> <dd>

Cerca nella directory specificata prima di cercare le directory specificate dalla variabile di ambiente INCLUDE.

</dd> <dt>

<span id="_j__loctype"></span><span id="_J__LOCTYPE"></span>**/j** *loctype*
</dt> <dd>

I tipi di risorse localizzabili RC inserisce in MUI (Language-Dependent Language-Dependent). FILE RES. Se è **impostata anche l'opzione /q,** questa opzione viene ignorata e le informazioni nel file di configurazione RC hanno la precedenza.

**Windows Server 2003 e Windows XP/2000:** Questa opzione non è disponibile senza usare anche le [**funzioni LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) e [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) in un sistema aggiornato.

</dd> <dt>

<span id="_k_overtype"></span><span id="_K_OVERTYPE"></span>**/k** *overtype*
</dt> <dd>

Tipi di risorse sovrapposti che RC inserisce in entrambi i tipi indipendenti dal linguaggio. RES e MUI (Language-Dependent). File RES. I tipi di risorsa specificati **dall'opzione /k** devono essere un subset di quelli specificati dall'opzione **/j.** Per esempio? J2 ? J3 ? K3 specifica che RC inserisce il tipo di risorsa 3 nei file muI (Language Neutral Language Neutral) e Language-Dependent (MUI). Se è **impostata anche l'opzione /q,** questa opzione viene ignorata e le informazioni nel file di configurazione RC hanno la precedenza.

**Windows Server 2003 e Windows XP/2000:** Questa opzione non è disponibile senza usare anche le [**funzioni LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) e [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) in un sistema aggiornato.

</dd> <dt>

<span id="_l_langid"></span><span id="_L_LANGID"></span>**/l** *langid*
</dt> <dd>

Specifica il linguaggio predefinito per la compilazione. Ad esempio, -l409 equivale a includere l'istruzione seguente all'inizio del file di script di risorsa: `LANGUAGE LANG_ENGLISH,SUBLANG_ENGLISH_US`

Per altre informazioni, vedere [Identificatori di lingua](/windows/desktop/Intl/language-identifiers).

</dd> <dt>

<span id="_n"></span><span id="_N"></span>**/n**
</dt> <dd>

Null termina tutte le stringhe nella tabella delle stringhe.

</dd> <dt>

<span id="_q_Mui.RCConfig"></span><span id="_q_mui.rcconfig"></span><span id="_Q_MUI.RCCONFIG"></span>**/q** *Mui.RCConfig*
</dt> <dd>

Un file di configurazione RC che segue il formato del file di configurazione RC. Il formato del file di configurazione RC consente ai componenti di descrivere autonomamente le informazioni sulle risorse, ad esempio il controllo delle versioni delle risorse, il percorso del file MUI, i tipi di risorse e gli elementi. Questo file specifica le risorse che passano all'oggetto indipendente dalla lingua. RES e le risorse che passano al file MUI (Language-Dependent Language- Dependent Language). FILE RES. Questa opzione e le informazioni fornite nel file di configurazione RC eseguono l'override delle opzioni della riga di comando **/j** e **/k**.

**Windows Server 2003 e Windows XP/2000:** Questa opzione non è disponibile senza usare anche le [**funzioni LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) e [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) in un sistema aggiornato.

</dd> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

Ignorato. Fornito per la compatibilità con i makefile esistenti.

</dd> <dt>

<span id="_u"></span><span id="_U"></span>**/u**
</dt> <dd>

Annulla la ridefinizione di un simbolo per il preprocessore.

</dd> <dt>

<span id="_v"></span><span id="_V"></span>**/v**
</dt> <dd>

Visualizza i messaggi che segnalano lo stato del compilatore.

</dd> <dt>

<span id="_x"></span><span id="_X"></span>**/x**
</dt> <dd>

Impedisce a RC di controllare la variabile di ambiente INCLUDE durante la ricerca di file di intestazione o di risorse.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le opzioni non supportano la distinzione tra maiuscole e minuscole e è possibile usare un trattino (-) al posto di una barra (/). È possibile combinare le opzioni di una sola lettera se non richiedono parametri aggiuntivi.

RC non genererà un file MUI nei casi seguenti.

-   Nel file RC non sono presenti risorse localizzabili.
-   L'unico ID lingua della risorsa specificato nel file RC è neutro (0x0).
-   Il file RC contiene risorse specificate in più lingue. L'eccezione è se il file RC contiene due lingue e una lingua è neutra (0x0), RC genera un file MUI.

Per altre informazioni, vedere i seguenti argomenti:

-   [Definizione dei nomi per il preprocessore](defining-names-for-the-preprocessor.md)
-   [Ridenominazione del file di risorse compilato](renaming-the-compiled-resource-file.md)
-   [Ricerca di file](searching-for-files.md)
-   [Visualizzazione di messaggi di stato](displaying-progress-messages.md)
-   [Messaggi di diagnostica RC](rc-diagnostic-messages.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfaccia utente multilingue](/windows/desktop/Intl/multilingual-user-interface)
</dt> </dl>

 

 