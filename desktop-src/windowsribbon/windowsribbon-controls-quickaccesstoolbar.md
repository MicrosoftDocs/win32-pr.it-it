---
title: Barra di accesso rapido
description: La barra di accesso rapido (QAT) è una piccola barra degli strumenti personalizzabile che espone un set di comandi specificati dall'applicazione o selezionati dall'utente.
ms.assetid: b2adf4e9-0de1-4c4d-9293-693d0f7cf6fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a50d562477e5c626d2d2bffa8ee5e0ecc84919
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046761"
---
# <a name="quick-access-toolbar"></a>Barra di accesso rapido

La barra di accesso rapido (QAT) è una piccola barra degli strumenti personalizzabile che espone un set di comandi specificati dall'applicazione o selezionati dall'utente.

- [Introduzione](#introduction)
- [Implementare la barra di accesso rapido](#implement-the-quick-access-toolbar)
  - [markup](#markup)
  - [Codice](#code)
- [Persistenza QAT](#qat-persistence)
- [Proprietà della barra di accesso rapido](#quick-access-toolbar-properties)
- [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

Per impostazione predefinita, la barra di accesso rapido (QAT) si trova nella barra del titolo della finestra dell'applicazione, ma può essere configurata per la visualizzazione sotto la barra multifunzione. Oltre a esporre i comandi, la barra di accesso rapido (QAT) include anche un menu a discesa personalizzabile che contiene il set completo di comandi QAT (default Quick Access Toolbar), sia nascosti che visualizzati nella barra di accesso rapido (QAT), e un set di barre di accesso rapido (QAT) e opzioni della barra multifunzione.

Lo screenshot seguente mostra un esempio della barra di accesso rapido della barra multifunzione (QAT).

![Screenshot di QAT nella barra multifunzione di Microsoft Paint.](images/markup/qat-and-menu.png)

La barra di accesso rapido (QAT) è costituita da una combinazione di un massimo di 20 comandi specificati dall'applicazione, noti come elenco di impostazioni predefinite dell'applicazione, o selezionati dall'utente. La barra di accesso rapido (QAT) può contenere comandi univoci che non sono disponibili altrove nell'interfaccia utente della barra multifunzione.

> [!Note]
> Sebbene quasi tutti i controlli della barra multifunzione consentano l'aggiunta del comando associato alla barra di accesso rapido (QAT) tramite il menu di scelta rapida illustrato nello screenshot seguente, i comandi esposti in una [finestra popup del contesto](windowsribbon-controls-contextpopup.md) non forniscono questo menu di scelta rapida.
>
> ![screenshot del menu di scelta rapida del comando sulla barra multifunzione di Microsoft Paint.](images/controls/qat-contextmenu-add.png) 

## <a name="implement-the-quick-access-toolbar"></a>Implementare la barra di accesso rapido

Come per tutti i controlli del Framework della barra multifunzione di Windows, per sfruttare appieno la barra di accesso rapido (QAT) è necessario un componente di markup che controlla la presentazione all'interno della barra multifunzione e un componente di codice che ne governa la funzionalità.

### <a name="markup"></a>markup

Il controllo barra di accesso rapido (QAT) viene dichiarato e associato a un ID di comando nel markup tramite l'elemento [QuickAccessToolBar](windowsribbon-element-quickaccesstoolbar.md) . L'ID di comando viene usato per identificare e associare la barra di accesso rapido (QAT) a un gestore di comando definito dall'applicazione.

Oltre al gestore dei comandi di base per la funzionalità della barra di accesso rapido principale (QAT), la dichiarazione dell'attributo facoltativo *CustomizeCommandName* [QuickAccessToolBar](windowsribbon-element-quickaccesstoolbar.md) Element fa in modo che il Framework aggiunga un **ulteriore elemento Commands** all'elenco dei comandi del menu a discesa della barra di accesso rapido (QAT) che richiede la definizione di un gestore di comando secondario.

Per coerenza tra le applicazioni della barra multifunzione, è consigliabile che il gestore di comandi *CustomizeCommandName* avvii una finestra di dialogo di personalizzazione della barra di accesso rapido (QAT). Poiché il Framework della barra multifunzione fornisce solo il punto di avvio nell'interfaccia utente, l'applicazione è responsabile esclusivamente di fornire l'implementazione della finestra di dialogo di personalizzazione quando viene ricevuta la notifica di callback per questo comando.

Lo screenshot seguente mostra un menu a discesa della barra di accesso rapido (QAT) con l'elemento di comando **altri comandi** .

![Screenshot di un menu qat con altri comandi... elemento del comando.](images/markup/qat-customizecommandname.png)

L'elenco delle impostazioni predefinite dell'applicazione per la barra di accesso rapido (QAT) viene specificato tramite la proprietà [QuickAccessToolBar. ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) , che identifica un elenco predefinito di comandi consigliati, tutti elencati nel menu a discesa della barra di accesso rapido (QAT).

Per visualizzare i comandi dall'elenco delle impostazioni predefinite dell'applicazione nella barra degli strumenti di accesso rapido (QAT), l'attributo *ApplicationDefaults. Dechecked* di ogni elemento del controllo deve avere un valore pari a `true` . Le immagini precedenti mostrano i risultati dell'impostazione di questo attributo su `true` per i comandi **Save**, **Undo** e **Redo** .

[QuickAccessToolBar. ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) supporta tre tipi di controlli della barra multifunzione: [Button](windowsribbon-controls-button.md), [interruttore](windowsribbon-controls-togglebutton.md)e [casella di controllo](windowsribbon-controls-checkbox.md).

> [!Note]
> Windows 8 e versioni successive: tutti i controlli basati su raccolta sono supportati ([ComboBox](windowsribbon-element-combobox.md), [inribbongallery](windowsribbon-element-inribbongallery.md), [SplitButtonGallery](windowsribbon-element-splitbuttongallery.md)e [DropDownGallery](windowsribbon-element-dropdowngallery.md)).
>
> Gli elementi in un controllo raccolta possono supportare l'evidenziazione al passaggio del mouse. Per supportare l'evidenziazione del passaggio del mouse, la raccolta deve essere una raccolta di elementi e usare un [FlowMenuLayout](windowsribbon-element-flowmenulayout.md) di tipo [VerticalMenuLayout](windowsribbon-element-verticalmenulayout.md).

Nell'esempio seguente viene illustrato il markup di base per un elemento [QuickAccessToolBar](windowsribbon-element-quickaccesstoolbar.md) .

In questa sezione del codice vengono illustrate le dichiarazioni di comando per un elemento [barra di accesso rapido (QAT)](windowsribbon-element-quickaccesstoolbar.md) .

```XML
<Command Name="cmdQAT"
         Symbol="ID_QAT"
         Id="40000"/>
<Command Name="cmdCustomizeQAT"
         Symbol="ID_CUSTOM_QAT"
         Id="40001"/>
```

In questa sezione del codice vengono illustrate le dichiarazioni di controllo per un elemento [barra di accesso rapido (QAT)](windowsribbon-element-quickaccesstoolbar.md) .

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

L'applicazione Ribbon Framework deve fornire un metodo di callback del gestore comandi per modificare la barra di accesso rapido (QAT). Questo gestore funziona in modo simile ai gestori della raccolta dei comandi, ad eccezione del fatto che la barra di accesso rapido (QAT) non supporta le categorie. Per ulteriori informazioni, vedere [utilizzo delle raccolte](ribbon-controls-galleries.md).

La raccolta di comandi della barra di accesso rapido (QAT) viene recuperata come oggetto [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) tramite la chiave della proprietà [ \_ \_ ItemsSource pkey dell'interfaccia utente](windowsribbon-reference-properties-uipkey-itemssource.md) . L'aggiunta di comandi alla barra di accesso rapido (QAT) in fase di esecuzione viene eseguita aggiungendo un oggetto [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) a **IUICollection**.

Diversamente dalle raccolte di comandi, non è necessaria una proprietà del tipo di comando ([UI \_ pkey \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md)) per l'oggetto [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) della barra di accesso rapido (QAT). Tuttavia, il comando deve esistere nella barra multifunzione o nell'elenco delle impostazioni di accesso rapido (QAT) dell'applicazione. non è possibile creare un nuovo comando in fase di esecuzione e aggiungerlo alla barra di accesso rapido (QAT).

> [!Note]  
> L'applicazione Ribbon non può sostituire la barra di accesso rapido (QAT) [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) con un oggetto raccolta personalizzato derivato da IEnumUnknown.

Nell'esempio seguente viene illustrata un'implementazione del gestore comando QAT (Basic Quick Access Toolbar).

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

Le impostazioni e gli elementi del comando della barra di accesso rapido (QAT) possono essere salvati in modo permanente tra le sessioni dell'applicazione usando le funzioni [IUIRibbon:: SaveSettingsToStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) e [IUIRibbon:: LoadSettingsFromStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) . Per ulteriori informazioni, vedere la pagina relativa [allo stato della barra multifunzione permanente](ribbon-statepersistence.md).

## <a name="quick-access-toolbar-properties"></a>Proprietà della barra di accesso rapido

Il Framework della barra multifunzione definisce una raccolta di [chiavi di proprietà](windowsribbon-reference-properties.md) per il controllo barra di accesso rapido (QAT).

In genere, una proprietà della barra di accesso rapido (QAT) viene aggiornata nell'interfaccia utente della barra multifunzione invalidando il comando associato al controllo tramite una chiamata al metodo [IUIFramework:: InvalidateUICommand](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . L'evento di invalidamento viene gestito e gli aggiornamenti delle proprietà definiti dal metodo di callback [IUICommandHandler:: UpdateProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

Il metodo di callback [IUICommandHandler:: UpdateProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e l'applicazione ha sottoposto a query un valore aggiornato della proprietà, fino a quando la proprietà non è richiesta dal Framework. Ad esempio, quando viene attivata una scheda e viene visualizzato un controllo nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.

> [!Note]  
> In alcuni casi, una proprietà può essere recuperata tramite il metodo [IUIFramework:: GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e impostata con il metodo [IUIFramework:: SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

Nella tabella seguente sono elencate le chiavi di proprietà associate al controllo barra di accesso rapido (QAT).

| Chiave della proprietà | Note |
|---|---|
| [Interfaccia utente \_ pkey \_ ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) | Supporta [IUIFramework:: GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) (non supporta [IUIFramework:: SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)). [IUIFramework:: GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) restituisce un puntatore a un oggetto IUICollection che rappresenta i comandi in qat. Ogni comando è identificato dal relativo ID di comando, ottenuto chiamando il metodo [IUISimplePropertySet:: GetValue](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) e passando l' [interfaccia utente della chiave \_ pkey \_ CommandID](windowsribbon-reference-properties-uipkey-commandid.md). |

Non sono presenti chiavi di proprietà associate all'elemento di comando **altri comandi** del menu a discesa della barra di accesso rapido (QAT)

## <a name="related-topics"></a>Argomenti correlati

- [Libreria di controlli Windows Ribbon Framework](windowsribbon-controls-entry.md)
- [Elemento di markup QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md)