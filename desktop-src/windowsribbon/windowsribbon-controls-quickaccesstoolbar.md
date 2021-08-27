---
title: Barra di accesso rapido
description: La barra di accesso rapido è una piccola barra degli strumenti personalizzabile che espone un set di comandi specificati dall'applicazione o selezionati dall'utente.
ms.assetid: b2adf4e9-0de1-4c4d-9293-693d0f7cf6fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d63eb3f7b1a2c1213430f86a9a12fe4517c738290ed736eb1d356420aa145cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110727"
---
# <a name="quick-access-toolbar"></a>Barra di accesso rapido

La barra di accesso rapido è una piccola barra degli strumenti personalizzabile che espone un set di comandi specificati dall'applicazione o selezionati dall'utente.

- [Introduzione](#introduction)
- [Implementare la barra di accesso rapido](#implement-the-quick-access-toolbar)
  - [markup](#markup)
  - [Codice](#code)
- [Persistenza QAT](#qat-persistence)
- [Proprietà della barra di accesso rapido](#quick-access-toolbar-properties)
- [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

Per impostazione predefinita, la barra di accesso rapido si trova nella barra del titolo della finestra dell'applicazione, ma può essere configurata per la visualizzazione sotto la barra multifunzione. Oltre a esporre i comandi, la barra di accesso rapido (QAT) include anche un menu a discesa personalizzabile che contiene il set completo di comandi predefiniti della barra di accesso rapido (QAT) (nascosti o visualizzati nella barra di accesso rapido) e un set di opzioni della barra di accesso rapido e della barra multifunzione.

La schermata seguente mostra un esempio della barra di accesso rapido della barra multifunzione.

![Screenshot della qat nella barra multifunzione di Microsoft Paint.](images/markup/qat-and-menu.png)

La barra di accesso rapido (QAT) è costituita da una combinazione di un massimo di 20 comandi specificati dall'applicazione (noti come elenco delle impostazioni predefinite dell'applicazione) o selezionati dall'utente. La barra di accesso rapido (QAT) può contenere comandi univoci che non sono disponibili altrove nell'interfaccia utente della barra multifunzione.

> [!Note]
> Sebbene quasi tutti i controlli della barra multifunzione consentano l'aggiunta del comando associato alla barra di accesso rapido tramite il menu di scelta rapida illustrato nello screenshot seguente, i comandi esposti in un [popup](windowsribbon-controls-contextpopup.md) di contesto non forniscono questo menu di scelta rapida.
>
> ![Screenshot del menu di scelta rapida dei comandi nella barra multifunzione di Microsoft Paint.](images/controls/qat-contextmenu-add.png) 

## <a name="implement-the-quick-access-toolbar"></a>Implementare la barra di accesso rapido

Come per tutti Windows controlli del framework della barra multifunzione, per sfruttare appieno la barra di accesso rapido (QAT) sono necessari sia un componente di markup che controlla la presentazione all'interno della barra multifunzione che un componente di codice che ne governa le funzionalità.

### <a name="markup"></a>markup

Il controllo Barra di accesso rapido (QAT) viene dichiarato e associato a un ID comando nel markup tramite [l'elemento QuickAccessToolbar.](windowsribbon-element-quickaccesstoolbar.md) L'ID comando viene usato per identificare e associare la barra di accesso rapido (QAT) a un gestore di comandi definito dall'applicazione.

Oltre al gestore comandi di base per la funzionalità principale della barra di accesso rapido (QAT), la dichiarazione dell'attributo dell'elemento *Facoltativo CustomizeCommandName* [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) fa sì che il framework aggiri un elemento Altri comandi all'elenco comandi del menu **a** discesa Della barra di accesso rapido che richiede la definizione di un gestore comandi secondario.

Per coerenza tra le applicazioni della barra multifunzione, è consigliabile che il gestore del comando *CustomizeCommandName* avvii una finestra di dialogo di personalizzazione della barra di accesso rapido. Poiché il framework della barra multifunzione fornisce solo il punto di avvio nell'interfaccia utente, l'applicazione è esclusivamente responsabile di fornire l'implementazione della finestra di dialogo di personalizzazione quando viene ricevuta la notifica di callback per questo comando.

La schermata seguente mostra un menu a discesa della barra di accesso rapido con **l'elemento Altri comandi.**

![Screenshot di un menu qat con altri comandi... elemento di comando.](images/markup/qat-customizecommandname.png)

L'elenco delle impostazioni predefinite dell'applicazione per la barra di accesso rapido viene specificato tramite la proprietà [QuickAccessToolbar.ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) che identifica un elenco predefinito di comandi consigliati, tutti elencati nel menu a discesa Della barra di accesso rapido.

Per visualizzare i comandi dall'elenco delle impostazioni predefinite dell'applicazione nella barra degli strumenti di accesso rapido, l'attributo *ApplicationDefaults.IsChecked* di ogni elemento di controllo deve avere un valore `true` . Le immagini precedenti mostrano i risultati dell'impostazione di questo attributo su per i comandi `true` **Save**, **Undo** e **Redo.**

[QuickAccessToolbar.ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) supporta tre tipi di controlli barra multifunzione: [Pulsante](windowsribbon-controls-button.md), [Interruttore](windowsribbon-controls-togglebutton.md)e [Casella di controllo](windowsribbon-controls-checkbox.md).

> [!Note]
> Windows 8 e versioni più nuove: sono supportati tutti i controlli basati sulla raccolta ([ComboBox](windowsribbon-element-combobox.md), [InRibbonGallery](windowsribbon-element-inribbongallery.md), [SplitButtonGallery](windowsribbon-element-splitbuttongallery.md)e [DropDownGallery](windowsribbon-element-dropdowngallery.md)).
>
> Gli elementi in un controllo raccolta possono supportare l'evidenziazione al passaggio del mouse. Per supportare l'evidenziazione al passaggio del mouse, la raccolta deve essere una raccolta di elementi e usare [un flowMenuLayout](windowsribbon-element-flowmenulayout.md) di tipo [VerticalMenuLayout](windowsribbon-element-verticalmenulayout.md).

L'esempio seguente illustra il markup di base per un [elemento QuickAccessToolbar.](windowsribbon-element-quickaccesstoolbar.md)

Questa sezione di codice illustra le dichiarazioni command per un elemento della barra di [accesso rapido.](windowsribbon-element-quickaccesstoolbar.md)

```XML
<Command Name="cmdQAT"
         Symbol="ID_QAT"
         Id="40000"/>
<Command Name="cmdCustomizeQAT"
         Symbol="ID_CUSTOM_QAT"
         Id="40001"/>
```

Questa sezione di codice illustra le dichiarazioni di controllo per un elemento della barra di [accesso rapido.](windowsribbon-element-quickaccesstoolbar.md)

```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```

### <a name="code"></a>Codice

L'applicazione del framework della barra multifunzione deve fornire un metodo di callback del gestore di comandi per modificare la barra di accesso rapido. Questo gestore funziona in modo simile ai gestori della raccolta di comandi, ad eccezione del fatto che la barra di accesso rapido non supporta le categorie. Per altre informazioni, vedere [Uso delle raccolte](ribbon-controls-galleries.md).

La raccolta command della barra di accesso rapido viene recuperata come oggetto [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) tramite la chiave della proprietà [ \_ \_ ItemsSource PKEY](windowsribbon-reference-properties-uipkey-itemssource.md) dell'interfaccia utente. L'aggiunta di comandi alla barra di accesso rapido (QAT) in fase di esecuzione viene eseguita aggiungendo un [oggetto IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) a **IUICollection**.

A differenza delle raccolte Command, una proprietà del tipo di comando ( UI PKEY CommandType ) non è necessaria per l'oggetto [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) della barra di accesso rapido.[ \_ \_ ](windowsribbon-reference-properties-uipkey-commandtype.md) Tuttavia, il comando deve esistere nell'elenco delle impostazioni predefinite della barra multifunzione o della barra di accesso rapido. Non è possibile creare un nuovo comando in fase di esecuzione e aggiungere alla barra di accesso rapido.

> [!Note]  
> L'applicazione barra multifunzione non può sostituire la barra di accesso rapido (QAT) [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) con un oggetto raccolta personalizzato derivato da IEnumUnknown.

L'esempio seguente illustra un'implementazione del gestore di comandi della barra di accesso rapido (QAT) di base.

```C++
/* QAT COMMAND HANDLER IMPLEMENTATION */
class CQATCommandHandler
      : public CComObjectRootEx<CComMultiThreadModel>
      , public IUICommandHandler
{
  public:
    BEGIN_COM_MAP(CQATCommandHandler)
      COM_INTERFACE_ENTRY(IUICommandHandler)
    END_COM_MAP()

    // QAT command handler's Execute method
    STDMETHODIMP Execute(UINT nCmdID,
                         UI_EXECUTIONVERB verb, 
                         const PROPERTYKEY* key,
                         const PROPVARIANT* ppropvarValue,
                         IUISimplePropertySet* pCommandExecutionProperties)
    {
      UNREFERENCED_PARAMETER(nCmdID);
      UNREFERENCED_PARAMETER(verb);
      UNREFERENCED_PARAMETER(ppropvarValue);
      UNREFERENCED_PARAMETER(pCommandExecutionProperties);

      // Do not expect Execute callback for a QAT command
      return E_NOTIMPL;
    }

    // QAT command handler's UpdateProperty method
    STDMETHODIMP UpdateProperty(UINT nCmdID,
                                REFPROPERTYKEY key,
                                const PROPVARIANT* ppropvarCurrentValue,
                                PROPVARIANT* ppropvarNewValue)
    {
      UNREFERENCED_PARAMETER(nCmdID);
      UNREFERENCED_PARAMETER(ppropvarNewValue);

      HRESULT hr = E_NOTIMPL;

      if (key == UI_PKEY_ItemsSource)
      {
        ATLASSERT(ppropvarCurrentValue->vt == VT_UNKNOWN);

        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        UINT nCount;
        if (SUCCEEDED(hr = spCollection->GetCount(&nCount)))
        {
          if (nCount == 0)
          {
            // If the current Qat list is empty, then we will add a few items here.
            UINT commands[] =  { cmdSave, cmdUndo};

            int count = _countof(commands);

            for (int i = 0; i < count; i++)
            {
              PROPERTYKEY keys[1] = {UI_PKEY_CommandId};
              CComObject<CItemProperties> *pItem = NULL;
              if (SUCCEEDED(CComObject<CItemProperties>::CreateInstance(&pItem)))
              {
                PROPVARIANT vars[1];

                InitPropVariantFromUInt32(commands[i], &vars[0]);

                pItem->Initialize(NULL, _countof(vars), keys, vars);

                CComPtr<IUnknown> spUnknown;
                pItem->QueryInterface(&spUnknown);
                spCollection->Add(spUnknown);
                            
                FreePropVariantArray(_countof(vars), vars);
              }
            }
          }
          else
          {
            // Do nothing if the Qat list is not empty.
            // Return S_FALSE to indicate the callback succeeded.
            return S_FALSE; 
          }
        }
      }
    return hr;
  }
};
```

## <a name="qat-persistence"></a>Persistenza QAT

Gli elementi e le impostazioni dei comandi della barra di accesso rapido possono essere resi persistenti tra le sessioni dell'applicazione usando le funzioni [IUIRibbon::SaveSettingsToStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) e [IUIRibbon::LoadSettingsFromStream.](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) Per altre informazioni, vedere [Persistenza dello stato della barra multifunzione.](ribbon-statepersistence.md)

## <a name="quick-access-toolbar-properties"></a>Proprietà della barra di accesso rapido

Il framework della barra multifunzione definisce una raccolta di chiavi [di proprietà](windowsribbon-reference-properties.md) per il controllo Barra di accesso rapido.

In genere, una proprietà della barra di accesso rapido viene aggiornata nell'interfaccia utente della barra multifunzione invalidando il comando associato al controllo tramite una chiamata al metodo [IUIFramework::InvalidateUICommand.](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) L'evento di invalidazione viene gestito e la proprietà viene aggiornata dal metodo di callback [IUICommandHandler::UpdateProperty.](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)

Il metodo di callback [IUICommandHandler::UpdateProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e l'applicazione ha eseguito una query per un valore di proprietà aggiornato, fino a quando la proprietà non è richiesta dal framework. Ad esempio, quando una scheda viene attivata e un controllo viene visualizzato nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.

> [!Note]  
> In alcuni casi, una proprietà può essere recuperata tramite il metodo [IUIFramework::GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e impostata con il metodo [IUIFramework::SetUICommandProperty.](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)

Nella tabella seguente sono elencate le chiavi di proprietà associate al controllo Barra di accesso rapido.

| Chiave di proprietà | Note |
|---|---|
| [Elementi \_ PKEY dell'interfaccia \_ utenteSource](windowsribbon-reference-properties-uipkey-itemssource.md) | Supporta [IUIFramework::GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) (non supporta [IUIFramework::SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)). [IUIFramework::GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) restituisce un puntatore a un oggetto IUICollection che rappresenta i comandi in QAT. Ogni comando è identificato dal relativo ID comando, ottenuto chiamando il metodo [IUISimplePropertySet::GetValue](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) e passando la chiave di proprietà [UI \_ PKEY \_ CommandId](windowsribbon-reference-properties-uipkey-commandid.md). |

Non sono presenti chiavi di proprietà associate alla **voce Altri** comandi del menu a discesa Della barra di accesso rapido

## <a name="related-topics"></a>Argomenti correlati

- [Windows Libreria di controlli Ribbon Framework](windowsribbon-controls-entry.md)
- [Elemento di markup QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md)